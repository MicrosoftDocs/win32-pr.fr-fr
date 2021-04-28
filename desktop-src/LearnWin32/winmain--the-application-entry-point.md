---
<span data-ttu-id="0af2c-101">title : WinMain le point d’entrée de l’application Description : WinMain : the application point Entry ms. AssetID : 389da5d4-d0f9-4339-BE6C-0f4fecc59316 ms. topic : article ms. Date : 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="0af2c-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="0af2c-102">WinMain : point d’entrée de l’application</span><span class="sxs-lookup"><span data-stu-id="0af2c-102">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="0af2c-103">Chaque programme Windows comprend une fonction de point d’entrée nommée **WinMain** ou **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="0af2c-103">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="0af2c-104">Voici la signature pour **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="0af2c-104">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="0af2c-105">Les quatre paramètres sont :</span><span class="sxs-lookup"><span data-stu-id="0af2c-105">The four parameters are:</span></span>

-   <span data-ttu-id="0af2c-106">*HINSTANCE* est un événement appelé « handle vers une instance » ou « handle vers un module ».</span><span class="sxs-lookup"><span data-stu-id="0af2c-106">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="0af2c-107">Le système d’exploitation utilise cette valeur pour identifier l’exécutable (EXE) lorsqu’il est chargé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="0af2c-107">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="0af2c-108">Le descripteur d’instance est nécessaire pour certaines fonctions Windows, par exemple pour charger des icônes ou des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="0af2c-108">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="0af2c-109">*hPrevInstance* n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="0af2c-109">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="0af2c-110">Elle a été utilisée dans Windows 16 bits, mais elle est désormais toujours égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="0af2c-110">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="0af2c-111">*pCmdLine* contient les arguments de ligne de commande sous la forme d’une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="0af2c-111">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="0af2c-112">*nCmdShow* est un indicateur qui indique si la fenêtre principale de l’application sera réduite, agrandie ou affichée normalement.</span><span class="sxs-lookup"><span data-stu-id="0af2c-112">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="0af2c-113">La fonction retourne une valeur **int** .</span><span class="sxs-lookup"><span data-stu-id="0af2c-113">The function returns an **int** value.</span></span> <span data-ttu-id="0af2c-114">La valeur de retour n’est pas utilisée par le système d’exploitation, mais vous pouvez utiliser la valeur de retour pour transmettre un code d’État à un autre programme que vous écrivez.</span><span class="sxs-lookup"><span data-stu-id="0af2c-114">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="0af2c-115">**WinAPI** est la Convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="0af2c-115">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="0af2c-116">Une *Convention d’appel* définit la manière dont une fonction reçoit des paramètres de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="0af2c-116">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="0af2c-117">Par exemple, il définit l’ordre dans lequel les paramètres apparaissent sur la pile.</span><span class="sxs-lookup"><span data-stu-id="0af2c-117">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="0af2c-118">Veillez simplement à déclarer votre fonction **wWinMain** comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="0af2c-118">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="0af2c-119">La fonction **WinMain** est identique à **wWinMain**, sauf que les arguments de ligne de commande sont passés comme une chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="0af2c-119">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="0af2c-120">La version Unicode est préférée.</span><span class="sxs-lookup"><span data-stu-id="0af2c-120">The Unicode version is preferred.</span></span> <span data-ttu-id="0af2c-121">Vous pouvez utiliser la fonction ANSI **WinMain** même si vous compilez votre programme au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="0af2c-121">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="0af2c-122">Pour obtenir une copie Unicode des arguments de ligne de commande, appelez la fonction [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="0af2c-122">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="0af2c-123">Cette fonction retourne tous les arguments dans une chaîne unique.</span><span class="sxs-lookup"><span data-stu-id="0af2c-123">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="0af2c-124">Si vous souhaitez que les arguments soient un tableau de style *argv*, transmettez cette chaîne à [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="0af2c-124">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="0af2c-125">Comment le compilateur sait-il appeler **wWinMain** au lieu de la fonction **principale** standard ?</span><span class="sxs-lookup"><span data-stu-id="0af2c-125">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="0af2c-126">Ce qui se passe réellement, c’est que la bibliothèque Microsoft C Runtime (CRT) fournit une implémentation de **main** qui appelle **WinMain** ou **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="0af2c-126">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="0af2c-127">La bibliothèque CRT effectue des tâches supplémentaires dans **main**.</span><span class="sxs-lookup"><span data-stu-id="0af2c-127">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="0af2c-128">Par exemple, tous les initialiseurs statiques sont appelés avant le **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="0af2c-128">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="0af2c-129">Bien que vous puissiez demander à l’éditeur de liens d’utiliser une fonction de point d’entrée différente, utilisez la valeur par défaut si vous liez à la bibliothèque CRT.</span><span class="sxs-lookup"><span data-stu-id="0af2c-129">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="0af2c-130">Sinon, le code d’initialisation du CRT sera ignoré, avec des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="0af2c-130">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="0af2c-131">(Par exemple, les objets globaux ne seront pas initialisés correctement.)</span><span class="sxs-lookup"><span data-stu-id="0af2c-131">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="0af2c-132">Voici une fonction **WinMain** vide.</span><span class="sxs-lookup"><span data-stu-id="0af2c-132">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="0af2c-133">Maintenant que vous disposez du point d’entrée et que vous comprenez certaines des conventions de base et de la terminologie de base, vous êtes prêt à créer un programme de fenêtre complet.</span><span class="sxs-lookup"><span data-stu-id="0af2c-133">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="0af2c-134">Suivant</span><span class="sxs-lookup"><span data-stu-id="0af2c-134">Next</span></span>

<span data-ttu-id="0af2c-135">[Module 1. Votre premier programme Windows](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="0af2c-135">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 
