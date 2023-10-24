# ap-git-handson
ap homework for getting to know Git and GitHub
<p>&nbsp;اول وارد دسکتاپ یا یک فضای مشخص شده سپس</p>
<p>یک دیرکتوری (پوشه) خالی به نام ap-git-handson بسازید و وارد آن شوید.</p>
<pre class="language-bash"><code>cd ~/Desktop
</code></pre>
<pre class="language-bash"><code>mkdir ap-git-handson</code></pre>
<pre class="language-bash"><code>cd ap-git-handson</code></pre>
<p>&nbsp;</p>
<p>با اجرای دستور git init دیرکتوری مذکور را تبدیل به یک Git Repository کنید.</p>
<pre class="language-bash"><code>git init</code></pre>
<p>با اجرای دستور ls -al از وجود دیرکتوری به نام git. مطمئن شوید.</p>
<pre class="language-bash"><code>ls -a / -al </code></pre>
<p>به کمک یک Text Editor تحت ترمینال مانند Vim یک فایل متنی به نام hello.c بسازید.</p>
<pre class="language-bash"><code>vi hello.c   /*or*/   vim hello.c   /*or*/   nano hello.c</code></pre>
<p>&nbsp;داخل این فایل برنامه زیر را نوشته، فایل را ذخیره کرده و از محیط ادیتور خارج شوید.</p>
<pre class="language-c"><code>#include &lt;stdio.h&gt;

int main()
{
    printf("Hello, World!");
    return 0;
}</code></pre>
<p>توجه: برای نوشتن در <code>vim</code> کلید <code>i</code> را زده و وارد حالت <code>insert</code> شوید&nbsp;<br />و برای جای گزاری متن کلید های <code>contrl +shift +v</code> را زده&nbsp;<br />حال برای ذخیره سازی اول با کلید <code>esc</code> از حالت <code>insert</code> خارج شده و با فشردن کلید&nbsp;<code> w + q + :</code> آن&nbsp; فایل را &zwnj;ذخیره کنید</p>
<p>سپس با اجرای دستور cat hello.c محتوای فایل را روی کنسول چاپ کنید.&nbsp;</p>
<pre class="language-bash"><code>cat hello.c</code></pre>

![shot1.png](../main/Screenshots/shot1.png)


<p>برای تمیز کردن ترمینال از دستور زیر استفاده میکنیم</p>
<pre class="language-bash"><code>clear</code></pre>
<p>&nbsp;با اجرای دستور git status وضعیت فایل&zwnj;ها در مخزن را مشاهده کنید.</p>
<pre class="language-bash"><code>git status</code></pre>
<p>فایل hello.c را به محیط Staging Area در گیت اضافه کنید.</p>
<pre class="language-bash"><code>git add hello.c</code></pre>
<p>&nbsp;یک کامیت با پیام initial commit بسازید</p>
<pre class="language-bash"><code>git commit -m "initial commit"</code></pre>
<p>توجه : اگر بار اول است که از گیت استفاده میکنید باید یوزر و ایمل خود رو با دستور زیر بزنید :</p>
<pre class="language-bash"><code>git config user.name "your_username"
git config user.email "your_email"</code></pre>
<p>&nbsp;با اجرای دستور git log مطمئن شوید که کامیت شما ثبت شده است.&nbsp;</p>
<pre class="language-bash"><code>git log </code></pre>
<p>توجه: برای خارج شدن از صفحه <code>log</code> میتوان از کلید <code>q</code> استفاده کرد&nbsp;</p>
<p>برای نشان دادن <code>log</code> در ترمینال میتوان از دستور زیر استفاده کرد&nbsp;</p>
<pre class="language-bash"><code>git log &gt; GitLog.txt &amp;&amp; cat GitLog.txt &amp;&amp; rm GitLog.txt</code></pre>

![shot2.png](../main/Screenshots/shot2.png)
<p>برای تمیز کردن ترمینال از دستور زیر استفاده میکنیم</p>
<pre class="language-bash"><code>clear</code></pre>
<p>&nbsp;</p>
<p><br />&nbsp;به وب&zwnj;سایت github.com رفته و یک اکانت برای خود بسازید و لاگین کنید. (در صورت مشکل برای ثبت نام و ورود، مشکل خود را در اینترنت جستجو کنید) &nbsp;سپس در بالا سمت چپ صفحه اصلی گیت&zwnj;هاب، روی دکمه New کلیک کنید و یک مخزن گیت ریموت به نام ap-git-handson روی اکانت گیت&zwnj;هاب خود بسازید. (نوع مخزن را Public انتخاب کنید که در دسترس عموم باشد، بخش Add a README file را تیک نزنید، بخش&zwnj;های Add .gitignore و Choose a licence را هم روی None قرار دهید) در ادامه آدرس مخزن گیت راه&zwnj;دور خود (Remote Git Repository) را از صفحه بعد کپی کنید.</p>
<p>&nbsp;به محیط ترمینال خود بازگشته و مخزن محلی (Local Repository) خود را به مخزن راه دور (Remote Repository) متصل کنید و نام این مخزن راه دور را origin بگذارید:</p>
<pre class="language-bash"><code>git remote add origin YOUR_REMOTE_REPOSITORY_ADDRESS</code></pre>
<p>کامیت&zwnj;های موجود در مخزن محلی خود را بر روی origin یا همان مخزن راه دور Push کنید.</p>
<pre class="language-bash"><code>git push origin main</code></pre>
<p>توجه: ممکن است نام برنچ اصلی شما main نباشد بلکه master باشد. برای رفع این مشکل علاوه برا این که کلمه main را به&nbsp; master تغیر داد میتوان از دستور زیر برنچ اصلی را به main تغیر داد :</p>
<pre class="language-bash"><code>git branch -M main</code></pre>
<p><br />توجه : در اینجا از شما یوزر و پسورد میخواهد : که یوزر شما همان یوزر گیت هاب است و پسورد شما از یک توکن مدت دار ساخته میشود&nbsp;<br />طریقه ساخت این توکن : در صفحه گیت هاب به گوشه صفحه که اواتار یوزر است کلیک کنید سپس وارد پنجره تنطیمات شده و در لیس کناری به پایین رفته&nbsp; و<code><a href="https://github.com/settings/apps">Developer Settings </a></code><a href="https://github.com/settings/apps"><span style="background-color: #fefefe; color: #323232; font-family: IRANYekan, Tahoma, Helvetica, sans-serif; font-size: 14px;">باز کرده&nbsp;</span></a> و سپس گزینه <code>Personal access tokens</code> را انتخاب میکنیم&nbsp; و در صفحه مورد نظر گزینه <code>Generate new token&nbsp;</code>&nbsp; حالت <code>classic</code> را انتخاب میکنیم سپس یک اسم انتخاب کرده و در قسمت پایین به این توکن دسترسی <code>repo</code> را میدهیم&nbsp; و در اخر صفحه <code>Generate token</code> را بزنید&nbsp; سپس توکن را در یک فایل ذخیره کنید</p>

![shot3.png](../main/Screenshots/shot3.png)
<p>&nbsp;به صفحه GitHub برگشته و آن را Refresh کنید تا فایل ها و کامیت&zwnj;های پوش شده را مشاهده کنید.</p>

![shot4.png](../main/Screenshots/shot4.png)
<p>برای تمیز کردن ترمینال از دستور زیر استفاده میکنیم</p>
<pre class="language-bash"><code>clear</code></pre>
<p>&nbsp;</p>
<p>&nbsp;فایل hello.c را در صفحه گیت&zwnj;هاب باز کرده و تغییری در آن اعمال کرده و نهایتا آن را ذخیره کنید. ذخیره از طریق صفحه&zwnj;ی گیت&zwnj;هاب به منزله&zwnj;ی یک کامیت جدید است.</p>
<p>به ترمینال برگشته و تغییراتی که از طریق صفحه&zwnj;ی گیت&zwnj;هاب روی پروژه اعمال شده را Pull میکنیم:</p>
<pre class="language-bash"><code>git pull origin main</code></pre>
<p>سپس برای اطمینان از pull شدن میتون از دستور زیر استفاده کرد :<br /><br /></p>
<pre class="language-bash"><code>cat hello.c
</code></pre>

![shot5.png](../main/Screenshots/shot5.png)
<p>برای تمیز کردن ترمینال از دستور زیر استفاده میکنیم</p>
<pre class="language-bash"><code>clear</code></pre>
<p>&nbsp;</p>
<p>&nbsp;در محیط ترمینال یک شاخه (Branch) جدید به نام java-version ساخته و آن را Checkout کنید.</p>
<pre class="language-bash"><code>git branch java-version 
git checkout java-version
</code></pre>
<p>یا با دستور ادغامی زیر هم یک branch&nbsp; بسازیم و chekout کنیم</p>
<pre class="language-bash"><code>git checkout -b java-version </code></pre>
<p>بعد از رفتن روی برنچ جدید، فایل hello.c را پاک کنید (توجه کنید که این فایل هم از Working Directory پاک شود و هم از Staging Area)</p>
<p>برای این کار میتوان از دو دستور&nbsp; زیر استفاده کنیم&nbsp;</p>
<pre class="language-bash"><code> git rm hello.c</code></pre>
<pre class="language-bash"><code>rm hello.c
git add hello.c</code></pre>
<p>برای اطمینان از حذف شدن درست فایل&nbsp; از دستور زیر استفاده میکنیم :</p>
<pre class="language-bash"><code>git status</code></pre>
<p>برای زیبای کار میتوان در این جا کامیت کرد :</p>
<pre class="language-bash"><code>git commit -m "delete hello.c"</code></pre>
<p>&nbsp;یک فایل جدید به نام Hello.java ساخته :</p>
<pre class="language-bash"><code>vim / vi / nano Hello.java </code></pre>
<p>و محتوای زیر را در آن کپی کنید:</p>
<pre class="language-java"><code>class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}</code></pre>
<p>&nbsp;فایل را ذخیره کرده و ان را cat میکنیم&nbsp;</p>
<pre class="language-bash"><code>cat Hello.java</code></pre>

![shot6.png](../main/Screenshots/shot6.png)
<p>برای تمیز کردن ترمینال از دستور زیر استفاده میکنیم</p>
<pre class="language-bash"><code>clear</code></pre>
<p>&nbsp;</p>
<p>در این جا با دستور</p>
<pre class="language-bash"><code>git add Hello.java</code></pre>
<p>&nbsp;فایل Hello.java را به گیت اضافه میکنیم و سپس ان را کامیت میکنیم&nbsp;</p>
<pre class="language-bash"><code>git commit -m "add Hello.java"</code></pre>
<p>مجددا به برنچ اصلی برگشته</p>
<pre class="language-bash"><code>git checkout main</code></pre>
<p>&nbsp;و برنچ java-version را روی آن ادغام (Merge) کنید.</p>
<pre class="language-bash"><code>git merge java-version</code></pre>
<p>در ترمینال فایل Hello.java به جای hello.c در برنج main امده ولی اگر صفحه گیت هاب خود را نگاه کنید متوجه میشوید که هنوز فایل hello.c در ان وجود&nbsp; دارد&nbsp; برای رفع این مشکل باید یک دور دستور زیر را اجرا کنید&nbsp;</p>
<pre class="language-bash"><code>git push origin main </code></pre>

![shot7.png](../main/Screenshots/shot7.png)
