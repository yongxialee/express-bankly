# In the middleware/auth.js file
- change decode() method to verify() and add SECRET_KEY
    let payload = jwt.verify(token,SECRET_KEY);
- change status code to 400
  401 is unauthorized 
  400 bad request response or missing require data
- import ExpressError 
    return next (new ExpressError("Unauthorized",401))