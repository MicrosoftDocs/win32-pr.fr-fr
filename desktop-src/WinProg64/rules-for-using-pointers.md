---
title: Règles d’utilisation des pointeurs
description: Le portage de votre code pour la compilation pour Microsoft Windows 32 et 64 bits est simple. Vous devez uniquement suivre quelques règles simples concernant les pointeurs de Cast et utiliser les nouveaux types de données dans votre code. Les règles de manipulation des pointeurs sont les suivantes.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- règles d’utilisation de la programmation Windows de pointeurs 64 bits
- manipulation de pointeur pour la programmation Windows 64 bits
- Programmation de pointeurs de casting Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103941435"
---
# <a name="rules-for-using-pointers"></a><span data-ttu-id="479ee-108">Règles d’utilisation des pointeurs</span><span class="sxs-lookup"><span data-stu-id="479ee-108">Rules for Using Pointers</span></span>

<span data-ttu-id="479ee-109">Le portage de votre code pour la compilation pour Microsoft Windows 32 et 64 bits est simple.</span><span class="sxs-lookup"><span data-stu-id="479ee-109">Porting your code to compile for both 32- and 64-bit Microsoft Windows is straightforward.</span></span> <span data-ttu-id="479ee-110">Vous devez uniquement suivre quelques règles simples concernant les pointeurs de Cast et utiliser les nouveaux types de données dans votre code.</span><span class="sxs-lookup"><span data-stu-id="479ee-110">You need only follow a few simple rules about casting pointers, and use the new data types in your code.</span></span> <span data-ttu-id="479ee-111">Les règles de manipulation des pointeurs sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="479ee-111">The rules for pointer manipulation are as follows.</span></span>

1.  <span data-ttu-id="479ee-112">N’effectuez pas de cast des pointeurs vers **int**, **long**, **ULong** ou **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="479ee-112">Do not cast pointers to **int**, **long**, **ULONG**, or **DWORD**.</span></span>

    <span data-ttu-id="479ee-113">Si vous devez effectuer un cast d’un pointeur pour tester certains bits, définir ou effacer des bits, ou encore manipuler son contenu, utilisez le type PTR **\_ ptr** ou **int \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="479ee-113">If you must cast a pointer to test some bits, set or clear bits, or otherwise manipulate its contents, use the **UINT\_PTR** or **INT\_PTR** type.</span></span> <span data-ttu-id="479ee-114">Ces types sont des types intégraux qui s’adaptent à la taille d’un pointeur pour les fenêtres 32 et 64 bits (par exemple, **ULong** pour les fenêtres 32 bits et \_ Int64 pour les fenêtres de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="479ee-114">These types are integral types that scale to the size of a pointer for both 32- and 64-bit Windows (for example, **ULONG** for 32-bit Windows and \_int64 for 64-bit Windows).</span></span> <span data-ttu-id="479ee-115">Par exemple, supposons que vous portiez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="479ee-115">For example, assume you are porting the following code:</span></span>

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    <span data-ttu-id="479ee-116">Dans le cadre du processus de Portage, vous devez modifier le code comme suit :</span><span class="sxs-lookup"><span data-stu-id="479ee-116">As a part of the porting process, you would change the code as follows:</span></span>

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    <span data-ttu-id="479ee-117">Utilisez **uint \_ ptr** et **int \_ ptr** le cas échéant (et si vous n’êtes pas certain qu’ils sont requis, il n’y a pas de danger de les utiliser uniquement dans le cas présent).</span><span class="sxs-lookup"><span data-stu-id="479ee-117">Use **UINT\_PTR** and **INT\_PTR** where appropriate (and if you are uncertain whether they are required, there is no harm in using them just in case).</span></span> <span data-ttu-id="479ee-118">N’effectuez pas de cast de vos pointeurs vers les types **ULong**, **long**, **int**, **uint** ou **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="479ee-118">Do not cast your pointers to the types **ULONG**, **LONG**, **INT**, **UINT**, or **DWORD**.</span></span>

    <span data-ttu-id="479ee-119">Notez que le **descripteur** est défini comme **\* void**, donc Cast une valeur de **handle** à une valeur **ULong** pour tester, définir ou décocher les bits de poids faible est une erreur sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="479ee-119">Note that **HANDLE** is defined as a **void\***, so typecasting a **HANDLE** value to a **ULONG** value to test, set, or clear the low-order 2 bits is an error on 64-bit Windows.</span></span>

2.  <span data-ttu-id="479ee-120">Utilisez la fonction **PtrToLong** ou **PtrToUlong** pour tronquer les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="479ee-120">Use the **PtrToLong** or **PtrToUlong** function to truncate pointers.</span></span>

    <span data-ttu-id="479ee-121">Si vous devez tronquer un pointeur vers une valeur 32 bits, utilisez la fonction **PtrToLong** ou **PtrToUlong** (définie dans Basetsd. h).</span><span class="sxs-lookup"><span data-stu-id="479ee-121">If you must truncate a pointer to a 32-bit value, use the **PtrToLong** or **PtrToUlong** function (defined in Basetsd.h).</span></span> <span data-ttu-id="479ee-122">Ces fonctions désactivent l’avertissement de troncation de pointeur pour la durée de l’appel.</span><span class="sxs-lookup"><span data-stu-id="479ee-122">These functions disable the pointer truncation warning for the duration of the call.</span></span>

    <span data-ttu-id="479ee-123">Utilisez ces fonctions avec précaution.</span><span class="sxs-lookup"><span data-stu-id="479ee-123">Use these functions carefully.</span></span> <span data-ttu-id="479ee-124">Une fois que vous avez converti une variable pointeur à l’aide de l’une de ces fonctions, ne l’utilisez jamais comme pointeur.</span><span class="sxs-lookup"><span data-stu-id="479ee-124">After you convert a pointer variable using one of these functions, never use it as a pointer again.</span></span> <span data-ttu-id="479ee-125">Ces fonctions tronquent les 32 bits supérieurs d’une adresse, qui sont généralement nécessaires pour accéder à la mémoire référencée à l’origine par le pointeur.</span><span class="sxs-lookup"><span data-stu-id="479ee-125">These functions truncate the upper 32 bits of an address, which are usually needed to access the memory originally referenced by pointer.</span></span> <span data-ttu-id="479ee-126">L’utilisation de ces fonctions sans tenir compte de la prudence entraînera un code fragile.</span><span class="sxs-lookup"><span data-stu-id="479ee-126">Using these functions without careful consideration will result in fragile code.</span></span>

3.  <span data-ttu-id="479ee-127">Soyez prudent lorsque vous utilisez \_ des valeurs de pointeur 32 dans du code qui peuvent être compilées en tant que code 64 bits.</span><span class="sxs-lookup"><span data-stu-id="479ee-127">Be careful when using POINTER\_32 values in code that may be compiled as 64-bit code.</span></span> <span data-ttu-id="479ee-128">Le compilateur signera l’extension du pointeur lorsqu’il sera assigné à un pointeur natif dans le code 64 bits, et non pas à l’extension du pointeur à zéro.</span><span class="sxs-lookup"><span data-stu-id="479ee-128">The compiler will sign-extend the pointer when it is assigned to a native pointer in 64-bit code, not zero-extend the pointer.</span></span>
4.  <span data-ttu-id="479ee-129">Soyez prudent lorsque vous utilisez \_ des valeurs de pointeur 64 dans du code qui peuvent être compilées en tant que code 32 bits.</span><span class="sxs-lookup"><span data-stu-id="479ee-129">Be careful when using POINTER\_64 values in code that may be compiled as 32-bit code.</span></span> <span data-ttu-id="479ee-130">Le compilateur signera l’extension du pointeur dans le code 32 bits, et non pas l’extension du pointeur à zéro.</span><span class="sxs-lookup"><span data-stu-id="479ee-130">The compiler will sign-extend the pointer in 32-bit code, not zero-extend the pointer.</span></span>
5.  <span data-ttu-id="479ee-131">Veillez à utiliser des paramètres OUT.</span><span class="sxs-lookup"><span data-stu-id="479ee-131">Be careful using OUT parameters.</span></span>

    <span data-ttu-id="479ee-132">Supposons, par exemple, que vous ayez défini une fonction comme suit :</span><span class="sxs-lookup"><span data-stu-id="479ee-132">For example, suppose you have a function defined as follows:</span></span>

    `void func( OUT PULONG *PointerToUlong );`

    <span data-ttu-id="479ee-133">N’appelez pas cette fonction comme suit.</span><span class="sxs-lookup"><span data-stu-id="479ee-133">Do not call this function as follows.</span></span>

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    <span data-ttu-id="479ee-134">Utilisez plutôt l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="479ee-134">Instead, use the following call.</span></span>

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    <span data-ttu-id="479ee-135">Cast &UL à **Pulong \*** empêche une erreur du compilateur, mais la fonction écrit une valeur de pointeur 64 bits dans la mémoire au niveau de &UL.</span><span class="sxs-lookup"><span data-stu-id="479ee-135">Typecasting &ul to **PULONG\*** prevents a compiler error, but the function will write a 64-bit pointer value into the memory at &ul.</span></span> <span data-ttu-id="479ee-136">Ce code fonctionne sur Windows 32 bits, mais entraîne une altération des données sur Windows 64 bits et il s’agit d’une corruption difficile et difficile à trouver.</span><span class="sxs-lookup"><span data-stu-id="479ee-136">This code works on 32-bit Windows, but will cause data corruption on 64-bit Windows and it will be subtle, hard-to-find corruption.</span></span> <span data-ttu-id="479ee-137">La ligne inférieure : ne jouez pas de plis avec le code C. la solution est plus simple et simple.</span><span class="sxs-lookup"><span data-stu-id="479ee-137">The bottom line: Do not play tricks with the C code—straightforward and simple is better.</span></span>

6.  <span data-ttu-id="479ee-138">Soyez vigilant avec les interfaces polymorphes.</span><span class="sxs-lookup"><span data-stu-id="479ee-138">Be careful with polymorphic interfaces.</span></span>

    <span data-ttu-id="479ee-139">Ne créez pas de fonctions qui acceptent des paramètres **DWORD** pour les données polymorphes.</span><span class="sxs-lookup"><span data-stu-id="479ee-139">Do not create functions that accept **DWORD** parameters for polymorphic data.</span></span> <span data-ttu-id="479ee-140">Si les données peuvent être un pointeur ou une valeur intégrale, utilisez le \_ type uint ptr ou **pVoid** .</span><span class="sxs-lookup"><span data-stu-id="479ee-140">If the data can be a pointer or an integral value, use the UINT\_PTR or **PVOID** type.</span></span>

    <span data-ttu-id="479ee-141">Par exemple, ne créez pas une fonction qui accepte un tableau de paramètres d’exception typés en tant que valeurs **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="479ee-141">For example, do not create a function that accepts an array of exception parameters typed as **DWORD** values.</span></span> <span data-ttu-id="479ee-142">Le tableau doit être un tableau de **valeurs \_ ptr DWORD** .</span><span class="sxs-lookup"><span data-stu-id="479ee-142">The array should be an array of **DWORD\_PTR** values.</span></span> <span data-ttu-id="479ee-143">Par conséquent, les éléments de tableau peuvent contenir des adresses ou des valeurs intégrales de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="479ee-143">Therefore, the array elements can hold addresses or 32-bit integral values.</span></span> <span data-ttu-id="479ee-144">(En règle générale, si le type d’origine est **DWORD** et qu’il doit être une largeur de pointeur, convertissez-le en valeur **\_ ptr DWORD** .</span><span class="sxs-lookup"><span data-stu-id="479ee-144">(The general rule is that if the original type is **DWORD** and it needs to be pointer width, convert it to a **DWORD\_PTR** value.</span></span> <span data-ttu-id="479ee-145">C’est pourquoi il existe des types de pointeurs de précision correspondants.) Si vous avez du code qui utilise des types **DWORD**, **ULong** ou d’autres types 32 bits de manière polymorphe (c’est-à-dire que vous voulez vraiment que le membre de la structure ou du paramètre contienne une adresse), utilisez **uint \_ ptr** à la place du type actuel.</span><span class="sxs-lookup"><span data-stu-id="479ee-145">That is why there are corresponding pointer-precision types.) If you have code that uses **DWORD**, **ULONG**, or other 32-bit types in a polymorphic way (that is, you really want the parameter or structure member to hold an address), use **UINT\_PTR** in place of the current type.</span></span>

7.  <span data-ttu-id="479ee-146">Utilisez les nouvelles fonctions de la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="479ee-146">Use the new window class functions.</span></span>

    <span data-ttu-id="479ee-147">Si vous avez des données privées de fenêtre ou de classe qui contiennent des pointeurs, votre code doit utiliser les nouvelles fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="479ee-147">If you have window or class private data that contains pointers, your code will need to use the following new functions:</span></span>

    -   [<span data-ttu-id="479ee-148">**GetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="479ee-148">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [<span data-ttu-id="479ee-149">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="479ee-149">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [<span data-ttu-id="479ee-150">**SetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="479ee-150">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [<span data-ttu-id="479ee-151">**SetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="479ee-151">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    <span data-ttu-id="479ee-152">Ces fonctions peuvent être utilisées sur les fenêtres 32 et 64 bits, mais elles sont requises sur les fenêtres 64 bits.</span><span class="sxs-lookup"><span data-stu-id="479ee-152">These functions can be used on both 32- and 64-bit Windows, but they are required on 64-bit Windows.</span></span> <span data-ttu-id="479ee-153">Préparez la transition à l’aide de ces fonctions maintenant.</span><span class="sxs-lookup"><span data-stu-id="479ee-153">Prepare for the transition by using these functions now.</span></span>

    <span data-ttu-id="479ee-154">En outre, vous devez accéder aux pointeurs ou aux handles dans les données privées de la classe à l’aide des nouvelles fonctions sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="479ee-154">Additionally, you must access pointers or handles in class private data using the new functions on 64-bit Windows.</span></span> <span data-ttu-id="479ee-155">Pour vous aider à trouver ces cas, les index suivants ne sont pas définis dans winuser. h pendant une compilation 64 bits :</span><span class="sxs-lookup"><span data-stu-id="479ee-155">To aid you in finding these cases, the following indexes are not defined in Winuser.h during a 64-bit compile:</span></span>

    -   <span data-ttu-id="479ee-156">GWL \_ WNDPROC</span><span class="sxs-lookup"><span data-stu-id="479ee-156">GWL\_WNDPROC</span></span>
    -   <span data-ttu-id="479ee-157">GWL \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="479ee-157">GWL\_HINSTANCE</span></span>
    -   <span data-ttu-id="479ee-158">GWL \_ HWDPARENT</span><span class="sxs-lookup"><span data-stu-id="479ee-158">GWL\_HWDPARENT</span></span>
    -   <span data-ttu-id="479ee-159">GWL \_ UserData</span><span class="sxs-lookup"><span data-stu-id="479ee-159">GWL\_USERDATA</span></span>

    <span data-ttu-id="479ee-160">Au lieu de cela, winuser. h définit les nouveaux index suivants :</span><span class="sxs-lookup"><span data-stu-id="479ee-160">Instead, Winuser.h defines the following new indexes:</span></span>

    -   <span data-ttu-id="479ee-161">GWLP \_ WNDPROC</span><span class="sxs-lookup"><span data-stu-id="479ee-161">GWLP\_WNDPROC</span></span>
    -   <span data-ttu-id="479ee-162">GWLP \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="479ee-162">GWLP\_HINSTANCE</span></span>
    -   <span data-ttu-id="479ee-163">GWLP \_ HWNDPARENT</span><span class="sxs-lookup"><span data-stu-id="479ee-163">GWLP\_HWNDPARENT</span></span>
    -   <span data-ttu-id="479ee-164">GWLP \_ UserData</span><span class="sxs-lookup"><span data-stu-id="479ee-164">GWLP\_USERDATA</span></span>
    -   <span data-ttu-id="479ee-165">\_ID GWLP</span><span class="sxs-lookup"><span data-stu-id="479ee-165">GWLP\_ID</span></span>

    <span data-ttu-id="479ee-166">Par exemple, le code suivant n’est pas compilé :</span><span class="sxs-lookup"><span data-stu-id="479ee-166">For example, the following code does not compile:</span></span>

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    <span data-ttu-id="479ee-167">Elle doit être modifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="479ee-167">It should be changed as follows:</span></span>

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    <span data-ttu-id="479ee-168">Lors de la définition du membre **cbWndExtra** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , veillez à réserver suffisamment d’espace pour les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="479ee-168">When setting the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure, be sure to reserve enough space for pointers.</span></span> <span data-ttu-id="479ee-169">Par exemple, si vous réservez actuellement des octets sizeof (DWORD) pour une valeur de pointeur, réservez les octets sizeof (DWORD \_ PTR).</span><span class="sxs-lookup"><span data-stu-id="479ee-169">For example, if you are currently reserving sizeof(DWORD) bytes for a pointer value, reserve sizeof(DWORD\_PTR) bytes.</span></span>

8.  <span data-ttu-id="479ee-170">Accédez à toutes les données de la fenêtre et de la classe à l’aide du **\_ décalage du champ**.</span><span class="sxs-lookup"><span data-stu-id="479ee-170">Access all window and class data using **FIELD\_OFFSET**.</span></span>

    <span data-ttu-id="479ee-171">Il est courant d’accéder aux données de fenêtre à l’aide d’offsets codés en dur.</span><span class="sxs-lookup"><span data-stu-id="479ee-171">It is common to access window data using hard-coded offsets.</span></span> <span data-ttu-id="479ee-172">Cette technique n’est pas portable pour Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="479ee-172">This technique is not portable to 64-bit Windows.</span></span> <span data-ttu-id="479ee-173">Pour rendre votre code portable, accédez à votre fenêtre et à vos données de classe à l’aide de la macro **\_ offset de champ** .</span><span class="sxs-lookup"><span data-stu-id="479ee-173">To make your code portable, access your window and class data using the **FIELD\_OFFSET** macro.</span></span> <span data-ttu-id="479ee-174">Ne partez pas du principe que le deuxième pointeur a un décalage de 4.</span><span class="sxs-lookup"><span data-stu-id="479ee-174">Do not assume that the second pointer has an offset of 4.</span></span>

9.  <span data-ttu-id="479ee-175">Les types **lParam**, **wParam** et **LRESULT** changent de taille avec la plateforme.</span><span class="sxs-lookup"><span data-stu-id="479ee-175">The **LPARAM**, **WPARAM**, and **LRESULT** types change size with the platform.</span></span>

    <span data-ttu-id="479ee-176">Lors de la compilation de code 64 bits, ces types sont étendus à 64 bits, car ils contiennent généralement des pointeurs ou des types intégraux.</span><span class="sxs-lookup"><span data-stu-id="479ee-176">When compiling 64-bit code, these types expand to 64 bits, because they typically hold pointers or integral types.</span></span> <span data-ttu-id="479ee-177">Ne combinez pas ces valeurs avec des valeurs **DWORD**, **ULong**, **uint**, **int**, **int** ou **long** .</span><span class="sxs-lookup"><span data-stu-id="479ee-177">Do not mix these values with **DWORD**, **ULONG**, **UINT**, **INT**, **int**, or **long** values.</span></span> <span data-ttu-id="479ee-178">Examinez la façon dont vous utilisez ces types et assurez-vous de ne pas tronquer par inadvertance les valeurs.</span><span class="sxs-lookup"><span data-stu-id="479ee-178">Examine how you use these types and ensure that you do not inadvertently truncate values.</span></span>

 

 