# ProgrammingAssignment2
makeCacheMatrix <- function(b = matrix()) {
  m<-NULL
  set<-function(y){
  b<<-y
  m<<-NULL
}
get<-function() b
setmatrix<-function(solve) m<<- solve
getmatrix<-function() m
list(set=set, get=get,
   setmatrix=setmatrix,
   getmatrix=getmatrix)
}

cacheSolve <- function(b=matrix(), ...) {
    m<-b$getmatrix()
    if(!is.null(m)){
      message("getting cached data")
      return(m)
    }
matrix <- b$get()
m <- solve(matrix, ...)
    x$setmatrix(m)
    m
}
