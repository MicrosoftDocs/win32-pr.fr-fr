---
description: Handle d’une chaîne de Windows Runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516007"
---
# <a name="hstring"></a><span data-ttu-id="687fb-103">HSTRING</span><span class="sxs-lookup"><span data-stu-id="687fb-103">HSTRING</span></span>

<span data-ttu-id="687fb-104">Handle d’une chaîne de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="687fb-104">A handle to a Windows Runtime string.</span></span>


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a><span data-ttu-id="687fb-105">Notes</span><span class="sxs-lookup"><span data-stu-id="687fb-105">Remarks</span></span>

<span data-ttu-id="687fb-106">Utilisez **HSTRING** pour représenter des chaînes immuables dans le Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="687fb-106">Use **HSTRING** to represent immutable strings in the Windows Runtime.</span></span>

<span data-ttu-id="687fb-107">JavaScript et d’autres langages, tels que C \# et Microsoft Visual Basic, peuvent utiliser des chaînes qui sont représentées à l’aide de **HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="687fb-107">JavaScript and other languages, such as C\#, and Microsoft Visual Basic, can use strings that are represented by using **HSTRING**.</span></span> <span data-ttu-id="687fb-108">Le tableau suivant montre comment un **HSTRING** est représenté dans d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="687fb-108">The following table shows how an **HSTRING** is represented in other languages.</span></span>



| <span data-ttu-id="687fb-109">Langage de programmation</span><span class="sxs-lookup"><span data-stu-id="687fb-109">Programming Language</span></span>                                                                    | <span data-ttu-id="687fb-110">Représentation sous forme de chaîne</span><span class="sxs-lookup"><span data-stu-id="687fb-110">String Representation</span></span>                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="687fb-111">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="687fb-111">C++/WinRT</span></span>](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | <span data-ttu-id="687fb-112">[WinRT :: hstring](/uwp/cpp-ref-for-winrt/hstring) , classe</span><span class="sxs-lookup"><span data-stu-id="687fb-112">[winrt::hstring](/uwp/cpp-ref-for-winrt/hstring) class</span></span>     |
| <span data-ttu-id="687fb-113">Extensions de composant Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span><span class="sxs-lookup"><span data-stu-id="687fb-113">Visual C++ component extensions ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span></span> | <span data-ttu-id="687fb-114">[Platform :: String](/cpp/cppcx/platform-string-class) , classe</span><span class="sxs-lookup"><span data-stu-id="687fb-114">[Platform::String](/cpp/cppcx/platform-string-class) class</span></span> |
| <span data-ttu-id="687fb-115">JavaScript</span><span class="sxs-lookup"><span data-stu-id="687fb-115">JavaScript</span></span>                                                                              | <span data-ttu-id="687fb-116">String (objet)</span><span class="sxs-lookup"><span data-stu-id="687fb-116">String object</span></span>                                              |
| <span data-ttu-id="687fb-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="687fb-117">.NET Framework</span></span>                                                                          | <span data-ttu-id="687fb-118">System. String (classe)</span><span class="sxs-lookup"><span data-stu-id="687fb-118">System.String class</span></span>                                        |



 

<span data-ttu-id="687fb-119">Le descripteur **HSTRING** est un type de handle standard.</span><span class="sxs-lookup"><span data-stu-id="687fb-119">The **HSTRING** handle is a standard handle type.</span></span> <span data-ttu-id="687fb-120">Sémantiquement, un **HSTRING** contenant la valeur **null** représente la chaîne vide, qui se compose de caractères de contenu nuls et d’un caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="687fb-120">Semantically, an **HSTRING** containing the value **NULL** represents the empty string, which consists of zero content characters and a terminating **NULL** character.</span></span> <span data-ttu-id="687fb-121">La création d’une chaîne via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) avec zéro caractère génère la valeur de handle **null**.</span><span class="sxs-lookup"><span data-stu-id="687fb-121">Creating a string via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) with zero characters will produce the handle value **NULL**.</span></span> <span data-ttu-id="687fb-122">Lors de l’appel de [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) avec la valeur **null**, un pointeur vers une chaîne vide, suivi uniquement par le caractère de fin **nul** , est retourné.</span><span class="sxs-lookup"><span data-stu-id="687fb-122">When calling [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) with the value **NULL**, a pointer to an empty string followed only by the **NUL** terminating character will be returned.</span></span> <span data-ttu-id="687fb-123">Il n’existe aucune valeur distincte pour représenter un **HSTRING** qui n’est pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="687fb-123">No distinct value exists to represent an **HSTRING** that is uninitialized.</span></span>

<span data-ttu-id="687fb-124">Appelez la fonction [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) pour créer un **HSTRING**, puis appelez la fonction [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) pour libérer la référence à la mémoire des chaînes de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="687fb-124">Call the [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) function to create a new **HSTRING**, and call the [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) function to release the reference to the backing string memory.</span></span> <span data-ttu-id="687fb-125">Appelez la fonction [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) pour créer une référence de chaîne, qui est également appelée une *chaîne de passe rapide*.</span><span class="sxs-lookup"><span data-stu-id="687fb-125">Call the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function to create a string reference, which is also called a *fast-pass string*.</span></span>

<span data-ttu-id="687fb-126">Copiez un **HSTRING** en appelant la fonction [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .</span><span class="sxs-lookup"><span data-stu-id="687fb-126">Copy an **HSTRING** by calling the [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) function.</span></span>

<span data-ttu-id="687fb-127">Concaténer deux chaînes en appelant la fonction [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .</span><span class="sxs-lookup"><span data-stu-id="687fb-127">Concatenate two strings by calling the [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) function.</span></span>

<span data-ttu-id="687fb-128">Accédez à la mémoire de la chaîne de sauvegarde en appelant la fonction [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .</span><span class="sxs-lookup"><span data-stu-id="687fb-128">Access the backing string memory by calling the [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) function.</span></span>

<span data-ttu-id="687fb-129">**HSTRING** peut stocker et utiliser des caractères **null** incorporés.</span><span class="sxs-lookup"><span data-stu-id="687fb-129">**HSTRING** can store and use embedded **NUL** characters.</span></span> <span data-ttu-id="687fb-130">Utilisez la fonction [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) pour rechercher les caractères **null** incorporés avant d’utiliser des fonctions qui peuvent produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="687fb-130">Use the [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) function to check for embedded **NUL** characters before using any functions which may produce unexpected results.</span></span> <span data-ttu-id="687fb-131">Par exemple, la plupart des fonctions Windows utilisent **LPCWSTR** comme paramètre d’entrée, et elles calculent la longueur de la chaîne uniquement jusqu’à ce que la première valeur **null** soit rencontrée.</span><span class="sxs-lookup"><span data-stu-id="687fb-131">For example, most of the Windows functions use **LPCWSTR** as an input parameter, and they compute the length of the string only until the first **NUL** is encountered.</span></span>

<span data-ttu-id="687fb-132">La chaîne de sauvegarde doit rester immuable et se terminer par null.</span><span class="sxs-lookup"><span data-stu-id="687fb-132">The backing string must remain immutable and null-terminated.</span></span> <span data-ttu-id="687fb-133">Lorsque le code appelant crée une référence de chaîne à l’aide de la fonction [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , la mémoire qui contient la représentation sous forme de chaîne de stockage appartient à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="687fb-133">When calling code creates a string reference by using the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function, the memory containing the backing string representation is owned by the caller.</span></span> <span data-ttu-id="687fb-134">Le Windows Runtime s’appuie sur le contenu de la chaîne d’origine pour rester inchangé.</span><span class="sxs-lookup"><span data-stu-id="687fb-134">The Windows Runtime relies on the contents of the original string to remain unchanged.</span></span> <span data-ttu-id="687fb-135">Lors du passage d’une référence de chaîne dans le Windows Runtime, il incombe à l’appelant de s’assurer que le contenu de la chaîne est invariable et que **nul** se termine pendant la durée de l’appel.</span><span class="sxs-lookup"><span data-stu-id="687fb-135">When passing a string reference into the Windows Runtime, it is the caller’s responsibility to ensure that the string’s contents are unchanging and **NUL** terminated for the duration of the call.</span></span> <span data-ttu-id="687fb-136">Le Windows Runtime libère toutes les références à la référence de chaîne lorsque l’appel est retourné.</span><span class="sxs-lookup"><span data-stu-id="687fb-136">The Windows Runtime releases all references to the string reference when the call returns.</span></span>

<span data-ttu-id="687fb-137">Quand vous recevez un **HSTRING** en tant que paramètre de sortie, il est recommandé de définir le handle sur la **valeur null** lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="687fb-137">When you receive an **HSTRING** as an out parameter, it is good practice to set the handle to **NULL** when you are finished with it.</span></span>

<span data-ttu-id="687fb-138">Appelez la fonction [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) pour allouer une mémoire tampon de chaîne mutable que vous pouvez utiliser pour créer un **HSTRING** immuable.</span><span class="sxs-lookup"><span data-stu-id="687fb-138">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to allocate a mutable string buffer that you can use to create an immutable **HSTRING**.</span></span> <span data-ttu-id="687fb-139">Lorsque vous avez terminé de remplir la mémoire tampon, vous appelez la fonction [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) pour créer le **HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="687fb-139">When you have finished populating the buffer, you call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) function to create the **HSTRING**.</span></span> <span data-ttu-id="687fb-140">Ce modèle de construction en deux phases active une fonctionnalité similaire à un « générateur de chaîne ».</span><span class="sxs-lookup"><span data-stu-id="687fb-140">This two-phase construction pattern enables functionality that is similar to a "string builder."</span></span>

## <a name="requirements"></a><span data-ttu-id="687fb-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="687fb-141">Requirements</span></span>



| <span data-ttu-id="687fb-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="687fb-142">Requirement</span></span> | <span data-ttu-id="687fb-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="687fb-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="687fb-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="687fb-144">Minimum supported client</span></span><br/> | <span data-ttu-id="687fb-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="687fb-145">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="687fb-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="687fb-146">Minimum supported server</span></span><br/> | <span data-ttu-id="687fb-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="687fb-147">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="687fb-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="687fb-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="687fb-149"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="687fb-149"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="687fb-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="687fb-150">See also</span></span>

<dl> <span data-ttu-id="687fb-151"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="687fb-151"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="687fb-152">**WindowsCreateString**</span><span class="sxs-lookup"><span data-stu-id="687fb-152">**WindowsCreateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[<span data-ttu-id="687fb-153">**WindowsDeleteString**</span><span class="sxs-lookup"><span data-stu-id="687fb-153">**WindowsDeleteString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[<span data-ttu-id="687fb-154">**WindowsDuplicateString**</span><span class="sxs-lookup"><span data-stu-id="687fb-154">**WindowsDuplicateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[<span data-ttu-id="687fb-155">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="687fb-155">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
