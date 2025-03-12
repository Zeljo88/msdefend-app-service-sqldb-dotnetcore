using Microsoft.AspNetCore.Mvc;

[ApiController]
[Route("api/auth")]
public class AuthController : ControllerBase
{
    private static readonly string _validUsername = "admin";
    private static readonly string _validPassword = "Password123!";

    [HttpPost("login")]
    public IActionResult Login([FromBody] LoginRequest request)
    {
        if (request.Username == _validUsername && request.Password == _validPassword)
        {
            return Ok(new { message = "Login successful", token = "fake-jwt-token" });
        }
        else
        {
            return Unauthorized(new { message = "Invalid credentials" });
        }
    }
}

public class LoginRequest
{
    public string Username { get; set; }
    public string Password { get; set; }
}
