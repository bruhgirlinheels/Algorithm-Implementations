# Algorithm-Implementations
# Sorting Algorithms
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    else:
        pivot = arr.pop()
    greater = [x for x in arr if x > pivot]
    lesser = [x for x in arr if x <= pivot]
    return quick_sort(lesser) + [pivot] + quick_sort(greater)

def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        L = arr[:mid]
        R = arr[mid:]

        merge_sort(L)
        merge_sort(R)

        i = j = k = 0

        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1

        while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1

        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1
    return arr

# Searching Algorithms
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1

def binary_search(arr, x):
    l, r = 0, len(arr) - 1
    while l <= r:
        mid = l + (r - l) // 2
        if arr[mid] == x:
            return mid
        elif arr[mid] < x:
            l = mid + 1
        else:
            r = mid - 1
    return -1

# Graph Algorithms (Using Sorting)
def graph_algorithm_using_sort(arr, sort_function):
    # Sort and then perform a hypothetical graph operation
    sorted_arr = sort_function(arr)
    # Hypothetical operation: count unique elements (simplified example)
    unique_elements = len(set(sorted_arr))
    return unique_elements

# Dynamic Algorithms (Using Insertion Sort)
def dynamic_algorithm_using_insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
    # Hypothetical dynamic programming operation: find max difference (simplified)
    return arr[-1] - arr[0]

# Greedy Algorithms (Using Selection Sort)
def greedy_algorithm_using_selection_sort(arr):
    for i in range(len(arr)):
        min_idx = i
        for j in range(i+1, len(arr)):
            if arr[min_idx] > arr[j]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
    # Hypothetical greedy operation: sum first three smallest elements
    return sum(arr[:3])

# Geometric Algorithms (Hypothetical Implementations)
def range_sort(arr):
    # Simple range-based sorting (hypothetical)
    return sorted(arr)

def angular_sort(points):
    # Sort points based on angle from the origin (0, 0)
    import math
    points.sort(key=lambda point: math.atan2(point[1], point[0]))
    return points

# Example usage of the functions
data = [10, 5, 2, 8, 15, 2, 3, 12, 7, 9]
print("Bubble Sorted:", bubble_sort(data.copy()))
print("Quick Sorted:", quick_sort(data.copy()))
print("Merge Sorted:", merge_sort(data.copy()))
print("Linear Search (5):", linear_search(data, 5))
print("Binary Search (8):", binary_search(sorted(data), 8))
print("Graph Using Quick Sort:", graph_algorithm_using_sort(data, quick_sort))
print("Dynamic Using Insertion Sort:", dynamic_algorithm_using_insertion_sort(data.copy()))
