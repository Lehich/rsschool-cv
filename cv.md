#Rebkavets Aliaksei

##lehichh@gmail.com

##Software engineer Responsible for the support and development of logistics software, my functions are:
   * analysis and search for solutions to the tasks set by clients;
   * development of new and improvement of existing functionality;
   * development of software product code according to ready-made specifications;
   * formation of internal documentation based on the results of the work; 
   * analysis and optimization of the code to improve the quality and performance of the software.
   
##Skills:
   * work with a database of languages Vip, SQL;
   * work with version control system (SVN (tortoisesvn client), VSS);
   * development and support of functionality with complex logic in the ERP system.
   
## Code:
```
   @RequestMapping(value = "/clear", method = RequestMethod.POST)
    public String clearing(HttpServletRequest request, HttpSession session) {
    public String clearing(@RequestParam String clearTableName,
                           HttpServletRequest request,
                           HttpSession session,
                           Model model) {
        try {
            DatabaseManager manager = getManager(session);
            String clearTableName = request.getParameter("clearTableName");
            request.setAttribute("findTableName", clearTableName);
            model.addAttribute("findTableName", clearTableName);
            service.clear(manager, clearTableName);
            request.setAttribute("table", service.find(manager, clearTableName));
            model.addAttribute("table", service.find(manager, clearTableName));
            return "find";
        } catch (Exception e) {
            request.setAttribute("message", e.getMessage());
            model.addAttribute("message", e.getMessage());
            return "error";
        }
    }
    @RequestMapping(value = "/create", method = RequestMethod.GET)
    public String create(HttpSession session) {
        DatabaseManager manager = getManager(session);
        if ((manager == DatabaseManager.NULL) || (manager == null)) {
            session.setAttribute("fromPage", "/create");
            return "redirect:connect";
        }
        return "create";
    }
```
   
##Knowledge and courses: 
   * Juja.com: Java Core, JUnit, JDBC, Servlets, JSP, Spring IoC, Spring MVC, PostgreSQL;
   * Streamline: English (elementary A0 - intermediate B1).