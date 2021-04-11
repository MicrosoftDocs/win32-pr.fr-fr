---
title: Pratiques de codage COM
description: Cette rubrique décrit comment rendre votre code COM plus efficace et plus robuste.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102477"
---
# <a name="com-coding-practices"></a><span data-ttu-id="1adb9-103">Pratiques de codage COM</span><span class="sxs-lookup"><span data-stu-id="1adb9-103">COM Coding Practices</span></span>

<span data-ttu-id="1adb9-104">Cette rubrique décrit comment rendre votre code COM plus efficace et plus robuste.</span><span class="sxs-lookup"><span data-stu-id="1adb9-104">This topic describes ways to make your COM code more effective and robust.</span></span>

-   [<span data-ttu-id="1adb9-105">\_ \_ Opérateur uuidof</span><span class="sxs-lookup"><span data-stu-id="1adb9-105">The \_\_uuidof Operator</span></span>](/windows)
-   [<span data-ttu-id="1adb9-106">La \_ macro IID PPV \_ args</span><span class="sxs-lookup"><span data-stu-id="1adb9-106">The IID\_PPV\_ARGS Macro</span></span>](/windows)
-   [<span data-ttu-id="1adb9-107">Modèle SafeRelease</span><span class="sxs-lookup"><span data-stu-id="1adb9-107">The SafeRelease Pattern</span></span>](#the-saferelease-pattern)
-   [<span data-ttu-id="1adb9-108">Pointeurs intelligents COM</span><span class="sxs-lookup"><span data-stu-id="1adb9-108">COM Smart Pointers</span></span>](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a><span data-ttu-id="1adb9-109">\_ \_ Opérateur uuidof</span><span class="sxs-lookup"><span data-stu-id="1adb9-109">The \_\_uuidof Operator</span></span>

<span data-ttu-id="1adb9-110">Lorsque vous générez votre programme, vous pouvez recevoir des erreurs de l’éditeur de liens semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1adb9-110">When you build your program, you might get linker errors similar to the following:</span></span>

`unresolved external symbol "struct _GUID const IID_IDrawable"`

<span data-ttu-id="1adb9-111">Cette erreur signifie qu’une constante GUID a été déclarée avec une liaison externe (**extern**) et que l’éditeur de liens n’a pas pu trouver la définition de la constante.</span><span class="sxs-lookup"><span data-stu-id="1adb9-111">This error means that a GUID constant was declared with external linkage (**extern**), and the linker could not find the definition of the constant.</span></span> <span data-ttu-id="1adb9-112">La valeur d’une constante GUID est généralement exportée à partir d’un fichier de bibliothèque statique.</span><span class="sxs-lookup"><span data-stu-id="1adb9-112">The value of a GUID constant is usually exported from a static library file.</span></span> <span data-ttu-id="1adb9-113">Si vous utilisez Microsoft Visual C++, vous pouvez éviter d’avoir à lier une bibliothèque statique à l’aide de l’opérateur **\_ \_ uuidof** .</span><span class="sxs-lookup"><span data-stu-id="1adb9-113">If you are using Microsoft Visual C++, you can avoid the need to link a static library by using the **\_\_uuidof** operator.</span></span> <span data-ttu-id="1adb9-114">Cet opérateur est une extension de langage Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1adb9-114">This operator is a Microsoft language extension.</span></span> <span data-ttu-id="1adb9-115">Elle retourne une valeur GUID à partir d’une expression.</span><span class="sxs-lookup"><span data-stu-id="1adb9-115">It returns a GUID value from an expression.</span></span> <span data-ttu-id="1adb9-116">L’expression peut être un nom de type interface, un nom de classe ou un pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="1adb9-116">The expression can be an interface type name, a class name, or an interface pointer.</span></span> <span data-ttu-id="1adb9-117">À l’aide de **\_ \_ uuidof**, vous pouvez créer l’objet de boîte de dialogue d’élément commun comme suit :</span><span class="sxs-lookup"><span data-stu-id="1adb9-117">Using **\_\_uuidof**, you can create the Common Item Dialog object as follows:</span></span>


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



<span data-ttu-id="1adb9-118">Le compilateur extrait la valeur GUID de l’en-tête, aucune exportation de bibliothèque n’est donc nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1adb9-118">The compiler extracts the GUID value from the header, so no library export is necessary.</span></span>

> [!Note]  
> <span data-ttu-id="1adb9-119">La valeur GUID est associée au nom de type en déclarant `__declspec(uuid( ... ))` dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="1adb9-119">The GUID value is associated with the type name by declaring `__declspec(uuid( ... ))` in the header.</span></span> <span data-ttu-id="1adb9-120">Pour plus d’informations, consultez la documentation relative à **\_ \_ declspec** dans la documentation Visual C++.</span><span class="sxs-lookup"><span data-stu-id="1adb9-120">For more information, see the documentation for **\_\_declspec** in the Visual C++ documentation.</span></span>

 

## <a name="the-iid_ppv_args-macro"></a><span data-ttu-id="1adb9-121">La \_ macro IID PPV \_ args</span><span class="sxs-lookup"><span data-stu-id="1adb9-121">The IID\_PPV\_ARGS Macro</span></span>

<span data-ttu-id="1adb9-122">Nous avons vu que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) et [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) requièrent la conversion du paramètre final en **type \* \* void** .</span><span class="sxs-lookup"><span data-stu-id="1adb9-122">We saw that both [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) require coercing the final parameter to a **void\*\*** type.</span></span> <span data-ttu-id="1adb9-123">Cela crée le risque d’incompatibilité de type.</span><span class="sxs-lookup"><span data-stu-id="1adb9-123">This creates the potential for a type mismatch.</span></span> <span data-ttu-id="1adb9-124">Prenons le fragment de code suivant :</span><span class="sxs-lookup"><span data-stu-id="1adb9-124">Consider the following code fragment:</span></span>


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



<span data-ttu-id="1adb9-125">Ce code demande l’interface [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , mais passe un pointeur [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="1adb9-125">This code asks for the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface, but passes in an [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer.</span></span> <span data-ttu-id="1adb9-126">L’expression de **\_ cast de réinterprétation** contourne le système de type C++, de sorte que le compilateur n’intercepte pas cette erreur.</span><span class="sxs-lookup"><span data-stu-id="1adb9-126">The **reinterpret\_cast** expression circumvents the C++ type system, so the compiler will not catch this error.</span></span> <span data-ttu-id="1adb9-127">Dans le meilleur des cas, si l’objet n’implémente pas l’interface demandée, l’appel échoue simplement.</span><span class="sxs-lookup"><span data-stu-id="1adb9-127">In the best case, if the object does not implement the requested interface, the call simply fails.</span></span> <span data-ttu-id="1adb9-128">Dans le pire des cas, la fonction s’exécute correctement et vous avez un pointeur incompatible.</span><span class="sxs-lookup"><span data-stu-id="1adb9-128">In the worst case, the function succeeds and you have a mismatched pointer.</span></span> <span data-ttu-id="1adb9-129">En d’autres termes, le type pointeur ne correspond pas à la vtable réelle en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1adb9-129">In other words, the pointer type does not match the actual vtable in memory.</span></span> <span data-ttu-id="1adb9-130">Comme vous pouvez l’imaginer, rien ne peut arriver à ce stade.</span><span class="sxs-lookup"><span data-stu-id="1adb9-130">As you can imagine, nothing good can happen at that point.</span></span>

> [!Note]  
> <span data-ttu-id="1adb9-131">Une table de méthodes virtuelles ( *vtable* ) est une table de pointeurs de fonction.</span><span class="sxs-lookup"><span data-stu-id="1adb9-131">A *vtable* (virtual method table) is a table of function pointers.</span></span> <span data-ttu-id="1adb9-132">La vtable est la manière dont COM lie un appel de méthode à son implémentation au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1adb9-132">The vtable is how COM binds a method call to its implementation at run time.</span></span> <span data-ttu-id="1adb9-133">Par contre, les vtables sont la manière dont la plupart des compilateurs C++ implémentent des méthodes virtuelles.</span><span class="sxs-lookup"><span data-stu-id="1adb9-133">Not coincidentally, vtables are how most C++ compilers implement virtual methods.</span></span>

 

<span data-ttu-id="1adb9-134">La macro [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) permet d’éviter cette classe d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1adb9-134">The [**IID\_PPV\_ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) macro helps to avoid this class of error.</span></span> <span data-ttu-id="1adb9-135">Pour utiliser cette macro, remplacez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="1adb9-135">To use this macro, replace the following code:</span></span>


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



<span data-ttu-id="1adb9-136">par le code :</span><span class="sxs-lookup"><span data-stu-id="1adb9-136">with this:</span></span>


```C++
IID_PPV_ARGS(&pFileOpen)
```



<span data-ttu-id="1adb9-137">La macro insère automatiquement `__uuidof(IFileOpenDialog)` pour l’identificateur d’interface. il est donc garanti qu’elle correspond au type de pointeur.</span><span class="sxs-lookup"><span data-stu-id="1adb9-137">The macro automatically inserts `__uuidof(IFileOpenDialog)` for the interface identifier, so it is guaranteed to match the pointer type.</span></span> <span data-ttu-id="1adb9-138">Voici le code modifié (et correct) :</span><span class="sxs-lookup"><span data-stu-id="1adb9-138">Here is the modified (and correct) code:</span></span>


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



<span data-ttu-id="1adb9-139">Vous pouvez utiliser la même macro avec [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="1adb9-139">You can use the same macro with [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a><span data-ttu-id="1adb9-140">Modèle SafeRelease</span><span class="sxs-lookup"><span data-stu-id="1adb9-140">The SafeRelease Pattern</span></span>

<span data-ttu-id="1adb9-141">Le décompte de références est l’un des éléments de la programmation qui est fondamentalement facile, mais qui est également fastidieux, ce qui facilite le problème.</span><span class="sxs-lookup"><span data-stu-id="1adb9-141">Reference counting is one of those things in programming that is basically easy, but is also tedious, which makes it easy to get wrong.</span></span> <span data-ttu-id="1adb9-142">Les erreurs sont généralement les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1adb9-142">Typical errors include:</span></span>

-   <span data-ttu-id="1adb9-143">Échec de la libération d’un pointeur d’interface lorsque vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="1adb9-143">Failing to release an interface pointer when you are done using it.</span></span> <span data-ttu-id="1adb9-144">Cette classe de bogue entraîne une fuite de mémoire et d’autres ressources par votre programme, car les objets ne sont pas détruits.</span><span class="sxs-lookup"><span data-stu-id="1adb9-144">This class of bug will cause your program to leak memory and other resources, because objects are not destroyed.</span></span>
-   <span data-ttu-id="1adb9-145">Appel de la [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) avec un pointeur non valide.</span><span class="sxs-lookup"><span data-stu-id="1adb9-145">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with an invalid pointer.</span></span> <span data-ttu-id="1adb9-146">Par exemple, cette erreur peut se produire si l’objet n’a jamais été créé.</span><span class="sxs-lookup"><span data-stu-id="1adb9-146">For example, this error can happen if the object was never created.</span></span> <span data-ttu-id="1adb9-147">Cette catégorie de bogue entraîne probablement un blocage de votre programme.</span><span class="sxs-lookup"><span data-stu-id="1adb9-147">This category of bug will probably cause your program to crash.</span></span>
-   <span data-ttu-id="1adb9-148">Déréférencement d’un pointeur d’interface après l’appel de [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="1adb9-148">Dereferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called.</span></span> <span data-ttu-id="1adb9-149">Ce bogue peut provoquer le blocage de votre programme.</span><span class="sxs-lookup"><span data-stu-id="1adb9-149">This bug may cause your program to crash.</span></span> <span data-ttu-id="1adb9-150">Pire encore, cela peut entraîner un blocage aléatoire de votre programme, ce qui rend difficile le suivi de l’erreur d’origine.</span><span class="sxs-lookup"><span data-stu-id="1adb9-150">Worse, it may cause your program to crash at a random later time, making it hard to track down the original error.</span></span>

<span data-ttu-id="1adb9-151">Une façon d’éviter ces bogues consiste à appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) via une fonction qui libère le pointeur en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="1adb9-151">One way to avoid these bugs is to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) through a function that safely releases the pointer.</span></span> <span data-ttu-id="1adb9-152">Le code suivant illustre une fonction qui effectue cette opérations :</span><span class="sxs-lookup"><span data-stu-id="1adb9-152">The following code shows a function that does this:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



<span data-ttu-id="1adb9-153">Cette fonction prend un pointeur d’interface COM en tant que paramètre et effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1adb9-153">This function takes a COM interface pointer as a parameter and does the following:</span></span>

1.  <span data-ttu-id="1adb9-154">Vérifie si le pointeur a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-154">Checks whether the pointer is **NULL**.</span></span>
2.  <span data-ttu-id="1adb9-155">Appelle la [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) si le pointeur n’est pas **null**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-155">Calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) if the pointer is not **NULL**.</span></span>
3.  <span data-ttu-id="1adb9-156">Définit le pointeur sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-156">Sets the pointer to **NULL**.</span></span>

<span data-ttu-id="1adb9-157">Voici un exemple d’utilisation de `SafeRelease` :</span><span class="sxs-lookup"><span data-stu-id="1adb9-157">Here is an example of how to use `SafeRelease`:</span></span>


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



<span data-ttu-id="1adb9-158">Si [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) s’exécute correctement, l’appel à `SafeRelease` libère le pointeur.</span><span class="sxs-lookup"><span data-stu-id="1adb9-158">If [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) succeeds, the call to `SafeRelease` releases the pointer.</span></span> <span data-ttu-id="1adb9-159">Si **CoCreateInstance** échoue, *PFileOpen* conserve la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-159">If **CoCreateInstance** fails, *pFileOpen* remains **NULL**.</span></span> <span data-ttu-id="1adb9-160">La `SafeRelease` fonction vérifie cela et ignore l’appel à [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="1adb9-160">The `SafeRelease` function checks for this and skips the call to [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span>

<span data-ttu-id="1adb9-161">Il est également possible d’appeler `SafeRelease` plusieurs fois sur le même pointeur, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="1adb9-161">It is also safe to call `SafeRelease` more than once on the same pointer, as shown here:</span></span>


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a><span data-ttu-id="1adb9-162">Pointeurs intelligents COM</span><span class="sxs-lookup"><span data-stu-id="1adb9-162">COM Smart Pointers</span></span>

<span data-ttu-id="1adb9-163">La `SafeRelease` fonction est utile, mais elle vous oblige à vous souvenir de deux choses :</span><span class="sxs-lookup"><span data-stu-id="1adb9-163">The `SafeRelease` function is useful, but it requires you to remember two things:</span></span>

-   <span data-ttu-id="1adb9-164">Initialise chaque pointeur d’interface avec la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-164">Initialize every interface pointer to **NULL**.</span></span>
-   <span data-ttu-id="1adb9-165">Appelez `SafeRelease` avant que chaque pointeur soit hors de portée.</span><span class="sxs-lookup"><span data-stu-id="1adb9-165">Call `SafeRelease` before each pointer goes out of scope.</span></span>

<span data-ttu-id="1adb9-166">En tant que programmeur C++, vous pensez probablement que vous ne devriez pas avoir à vous souvenir de l’un de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="1adb9-166">As a C++ programmer, you are probably thinking that you shouldn't have to remember either of these things.</span></span> <span data-ttu-id="1adb9-167">Après tout, c’est pourquoi C++ a des constructeurs et des destructeurs.</span><span class="sxs-lookup"><span data-stu-id="1adb9-167">After all, that's why C++ has constructors and destructors.</span></span> <span data-ttu-id="1adb9-168">Il serait intéressant d’avoir une classe qui encapsule le pointeur d’interface sous-jacent et initialise et libère automatiquement le pointeur.</span><span class="sxs-lookup"><span data-stu-id="1adb9-168">It would be nice to have a class that wraps the underlying interface pointer and automatically initializes and releases the pointer.</span></span> <span data-ttu-id="1adb9-169">En d’autres termes, nous souhaitons obtenir ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1adb9-169">In other words, we want something like this:</span></span>


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



<span data-ttu-id="1adb9-170">La définition de classe présentée ici est incomplète et n’est pas utilisable comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="1adb9-170">The class definition shown here is incomplete, and is not usable as shown.</span></span> <span data-ttu-id="1adb9-171">Au minimum, vous devez définir un constructeur de copie, un opérateur d’assignation et un moyen d’accéder au pointeur COM sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="1adb9-171">At a minimum, you would need to define a copy constructor, an assignment operator, and a way to access the underlying COM pointer.</span></span> <span data-ttu-id="1adb9-172">Heureusement, vous n’avez pas besoin d’effectuer ce travail, car Microsoft Visual Studio fournit déjà une classe de pointeur intelligent dans le cadre de la Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="1adb9-172">Fortunately, you don't need to do any of this work, because Microsoft Visual Studio already provides a smart pointer class as part of the Active Template Library (ATL).</span></span>

<span data-ttu-id="1adb9-173">La classe de pointeur intelligent ATL est nommée **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-173">The ATL smart pointer class is named **CComPtr**.</span></span> <span data-ttu-id="1adb9-174">(Il existe également une classe **CComQIPtr** , qui n’est pas abordée ici.) Voici l’exemple de [boîte de dialogue Ouvrir](example--the-open-dialog-box.md) réécrit pour utiliser **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-174">(There is also a **CComQIPtr** class, which is not discussed here.) Here is the [Open Dialog Box](example--the-open-dialog-box.md) example rewritten to use **CComPtr**.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="1adb9-175">La principale différence entre ce code et l’exemple d’origine est que cette version n’appelle pas explicitement [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="1adb9-175">The main difference between this code and the original example is that this version does not explicitly call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="1adb9-176">Lorsque l’instance **CComPtr** est hors de portée, le destructeur appelle **Release** sur le pointeur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="1adb9-176">When the **CComPtr** instance goes out of scope, the destructor calls **Release** on the underlying pointer.</span></span>

<span data-ttu-id="1adb9-177">**CComPtr** est un modèle de classe.</span><span class="sxs-lookup"><span data-stu-id="1adb9-177">**CComPtr** is a class template.</span></span> <span data-ttu-id="1adb9-178">L’argument template est le type d’interface COM.</span><span class="sxs-lookup"><span data-stu-id="1adb9-178">The template argument is the COM interface type.</span></span> <span data-ttu-id="1adb9-179">En interne, **CComPtr** contient un pointeur de ce type.</span><span class="sxs-lookup"><span data-stu-id="1adb9-179">Internally, **CComPtr** holds a pointer of that type.</span></span> <span data-ttu-id="1adb9-180">**CComPtr** remplace **Operator-> ()** et **Operator& ()** afin que la classe agisse comme le pointeur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="1adb9-180">**CComPtr** overrides **operator->()** and **operator&()** so that the class acts like the underlying pointer.</span></span> <span data-ttu-id="1adb9-181">Par exemple, le code suivant est équivalent à l’appel direct de la méthode **IFileOpenDialog :: Show** :</span><span class="sxs-lookup"><span data-stu-id="1adb9-181">For example, the following code is equivalent to calling the **IFileOpenDialog::Show** method directly:</span></span>


```C++
hr = pFileOpen->Show(NULL);
```



<span data-ttu-id="1adb9-182">**CComPtr** définit également une méthode **CComPtr :: CoCreateInstance** , qui appelle la fonction com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec des valeurs de paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="1adb9-182">**CComPtr** also defines a **CComPtr::CoCreateInstance** method, which calls the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function with some default parameter values.</span></span> <span data-ttu-id="1adb9-183">Le seul paramètre obligatoire est l’identificateur de classe, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="1adb9-183">The only required parameter is the class identifier, as the next example shows:</span></span>


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



<span data-ttu-id="1adb9-184">La méthode **CComPtr :: CoCreateInstance** est fournie à titre purement pratique ; vous pouvez toujours appeler la fonction COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , si vous préférez.</span><span class="sxs-lookup"><span data-stu-id="1adb9-184">The **CComPtr::CoCreateInstance** method is provided purely as a convenience; you can still call the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, if you prefer.</span></span>

## <a name="next"></a><span data-ttu-id="1adb9-185">Suivant</span><span class="sxs-lookup"><span data-stu-id="1adb9-185">Next</span></span>

[<span data-ttu-id="1adb9-186">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="1adb9-186">Error Handling in COM</span></span>](error-handling-in-com.md)

 

 