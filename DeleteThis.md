import { test, expect } from '@playwright/test';

test('test', async ({ page }) => {
    await page.goto('https://www.naukri.com/');
    await page.getByRole('link', { name: 'Login', exact: true }).click();
    await page.getByRole('textbox', { name: 'Enter your active Email ID /' }).click();
    await page.getByRole('textbox', { name: 'Enter your active Email ID /' }).fill('anukalp@gmail.com');
    await page.getByRole('textbox', { name: 'Enter your password' }).click();
    await page.getByRole('textbox', { name: 'Enter your password' }).fill('');
    await page.getByRole('button', { name: 'Login', exact: true }).click();
    await page.getByRole('img', { name: 'naukri user profile img' }).click();
    await page.getByRole('link', { name: 'View & Update Profile' }).click();

    await page.locator("//li/span[contains(text(),'Profile summary')]").click();
    await page.locator("//span[contains(text(),'Profile summary')]/following-sibling::span").click();
    await page.locator("//span[contains(text(),'Profile summary')]/following-sibling::span[contains(text(),'Delete')]").click();
    await page.locator("(//button[@class='btn-dark-ot'])[4]").click();

    await page.locator("//span[contains(text(),'Profile summary')]/following-sibling:: a").click();
    await page.locator('.profileSummaryTxt').click();
    await page.locator('.profileSummaryTxt').fill("Test...Experienced DevOps/DevSecOps Engineer with expertise in automating processes, optimizing cloud infrastructure, and accelerating software delivery cycles. Skilled in CI/CD pipelines (Jenkins, ArgoCD), containerization (Docker, Kubernetes), and cloud platforms (AWS, Azure). Passionate about transforming manual workflows into efficient, automated processes and delivering secure, scalable solutions. Proficient in IaC (Terraform, Ansible), monitoring tools (Prometheus, Grafana), and scripting (Python, Shell, PowerShell). Thrive in dynamic environments, driving innovation and operational excellence.");
    await page.getByRole('button', { name: 'Save' }).click();
});
