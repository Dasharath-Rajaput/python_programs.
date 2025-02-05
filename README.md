Binary search using python.
======================== binary_search program ===========================
def binary_search(sorted_list,target):
left = 0
right = len(sorted_list)-1
while left<=right:
mid = (left + right)//2
   if sorted_list[mid]<target:
      left = mid+1
   elif sorted_list[mid]>target:
      right = mid-1
   else:
      return mid
return -1
sorted_list = [3,8,12,17,15,36,42,58,67,79]
target = 36
result = binary_search(sorted_list,target)
if result!= -1:
  print(f"the element:{target} is found at index no:{ result}:")
else:
  print("the element is not found")
