---
title: Conformité STRICTe
description: Un code source qui se compile correctement peut générer des messages d’erreur lorsque vous activez la vérification de type STRICTe.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382219"
---
# <a name="strict-compliance"></a><span data-ttu-id="151cf-103">Conformité STRICTe</span><span class="sxs-lookup"><span data-stu-id="151cf-103">STRICT Compliance</span></span>

<span data-ttu-id="151cf-104">Un code source qui se compile correctement peut générer des messages d’erreur lorsque vous activez la vérification de type **stricte** .</span><span class="sxs-lookup"><span data-stu-id="151cf-104">Some source code that compiles successfully might produce error messages when you enable **STRICT** type checking.</span></span> <span data-ttu-id="151cf-105">Les sections suivantes décrivent la configuration minimale requise pour la compilation de votre code lorsque **strict** est activé.</span><span class="sxs-lookup"><span data-stu-id="151cf-105">The following sections describe the minimal requirements for making your code compile when **STRICT** is enabled.</span></span> <span data-ttu-id="151cf-106">Des étapes supplémentaires sont recommandées, en particulier pour produire du code portable.</span><span class="sxs-lookup"><span data-stu-id="151cf-106">Additional steps are recommended, especially to produce portable code.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="151cf-107">Conditions générales requises</span><span class="sxs-lookup"><span data-stu-id="151cf-107">General Requirements</span></span>

<span data-ttu-id="151cf-108">La principale exigence est que vous devez déclarer des types de handle et des pointeurs de fonction corrects au lieu de vous appuyer sur des types plus généraux.</span><span class="sxs-lookup"><span data-stu-id="151cf-108">The principal requirement is that you must declare correct handle types and function pointers instead of relying on more general types.</span></span> <span data-ttu-id="151cf-109">Vous ne pouvez pas utiliser un type de handle dans lequel un autre est attendu.</span><span class="sxs-lookup"><span data-stu-id="151cf-109">You cannot use one handle type where another is expected.</span></span> <span data-ttu-id="151cf-110">Cela signifie également que vous devrez peut-être modifier les déclarations de fonction et utiliser d’autres casts de type.</span><span class="sxs-lookup"><span data-stu-id="151cf-110">This also means that you may have to change function declarations and use more type casts.</span></span>

<span data-ttu-id="151cf-111">Pour de meilleurs résultats, le type de **handle** générique doit être utilisé uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="151cf-111">For best results, the generic **HANDLE** type should be used only when necessary.</span></span>

## <a name="declaring-functions-within-your-application"></a><span data-ttu-id="151cf-112">Déclaration de fonctions dans votre application</span><span class="sxs-lookup"><span data-stu-id="151cf-112">Declaring Functions Within Your Application</span></span>

<span data-ttu-id="151cf-113">Assurez-vous que toutes les fonctions d’application sont déclarées.</span><span class="sxs-lookup"><span data-stu-id="151cf-113">Make sure all application functions are declared.</span></span> <span data-ttu-id="151cf-114">Il est recommandé de placer toutes les déclarations de fonction dans un fichier include, car vous pouvez facilement analyser vos déclarations et rechercher les types de paramètres et de retour qui doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="151cf-114">Placing all function declarations in an include file is recommended because you can easily scan your declarations and look for parameter and return types that should be changed.</span></span>

<span data-ttu-id="151cf-115">Si vous utilisez l’option de compilateur **/ZG** pour créer des fichiers d’en-tête pour vos fonctions, n’oubliez pas que vous obtiendrez des résultats différents selon que vous avez activé la vérification de type **stricte** .</span><span class="sxs-lookup"><span data-stu-id="151cf-115">If you use the **/Zg** compiler option to create header files for your functions, remember that you will get different results depending on whether you have enabled **STRICT** type checking.</span></span> <span data-ttu-id="151cf-116">Si la fonction **strict** est désactivée, tous les types de handles génèrent le même type de base.</span><span class="sxs-lookup"><span data-stu-id="151cf-116">With **STRICT** disabled, all handle types generate the same base type.</span></span> <span data-ttu-id="151cf-117">Si l’option **strict** est activée, elles génèrent des types de base différents.</span><span class="sxs-lookup"><span data-stu-id="151cf-117">With **STRICT** enabled, they generate different base types.</span></span> <span data-ttu-id="151cf-118">Pour éviter les conflits, vous devez recréer le fichier d’en-tête chaque fois que vous activez ou désactivez **strict**, ou modifiez le fichier d’en-tête pour utiliser les types **HWND**, **HDC**, **handle**, etc., au lieu des types de base.</span><span class="sxs-lookup"><span data-stu-id="151cf-118">To avoid conflict, you need to re-create the header file each time you enable or disable **STRICT**, or edit the header file to use the types **HWND**, **HDC**, **HANDLE**, and so on, instead of the base types.</span></span>

<span data-ttu-id="151cf-119">Toutes les déclarations de fonction que vous avez copiées à partir de Windows. h dans votre code source ont peut-être changé et votre déclaration locale peut être obsolète.</span><span class="sxs-lookup"><span data-stu-id="151cf-119">Any function declarations that you copied from Windows.h into your source code may have changed, and your local declaration may be out of date.</span></span> <span data-ttu-id="151cf-120">Supprimez votre déclaration locale.</span><span class="sxs-lookup"><span data-stu-id="151cf-120">Remove your local declaration.</span></span>

## <a name="types-that-require-casts"></a><span data-ttu-id="151cf-121">Types qui requièrent des casts</span><span class="sxs-lookup"><span data-stu-id="151cf-121">Types that Require Casts</span></span>

<span data-ttu-id="151cf-122">Certaines fonctions ont des paramètres ou des types de retour génériques.</span><span class="sxs-lookup"><span data-stu-id="151cf-122">Some functions have generic return types or parameters.</span></span> <span data-ttu-id="151cf-123">Par exemple, la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) retourne des données qui peuvent être de n’importe quel nombre de types, en fonction du contexte.</span><span class="sxs-lookup"><span data-stu-id="151cf-123">For example, the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function returns data that may be any number of types, depending on the context.</span></span> <span data-ttu-id="151cf-124">Lorsque vous voyez l’une de ces fonctions dans votre code source, assurez-vous que vous utilisez la conversion de type correcte et qu’elle est la plus spécifique possible.</span><span class="sxs-lookup"><span data-stu-id="151cf-124">When you see any of these functions in your source code, make sure that you use the correct type cast and that it is as specific as possible.</span></span> <span data-ttu-id="151cf-125">La liste suivante est un exemple de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="151cf-125">The following list is an example of these functions.</span></span>

-   [<span data-ttu-id="151cf-126">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="151cf-126">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [<span data-ttu-id="151cf-127">**GlobalLock**</span><span class="sxs-lookup"><span data-stu-id="151cf-127">**GlobalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [<span data-ttu-id="151cf-128">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="151cf-128">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [<span data-ttu-id="151cf-129">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="151cf-129">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [<span data-ttu-id="151cf-130">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="151cf-130">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="151cf-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="151cf-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [<span data-ttu-id="151cf-132">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="151cf-132">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

<span data-ttu-id="151cf-133">Quand vous appelez [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)ou [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), vous devez d’abord convertir le résultat en type **uint \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="151cf-133">When you call [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), or [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), you should first cast the result to type **UINT\_PTR**.</span></span> <span data-ttu-id="151cf-134">Vous devez effectuer des étapes similaires pour toute fonction qui retourne une valeur **LRESULT** ou **long \_ ptr** , où le résultat contient un descripteur.</span><span class="sxs-lookup"><span data-stu-id="151cf-134">You need to take similar steps for any function that returns an **LRESULT** or **LONG\_PTR** value, where the result contains a handle.</span></span> <span data-ttu-id="151cf-135">Cela est nécessaire pour écrire du code portable, car la taille d’une poignée varie selon la version de Windows.</span><span class="sxs-lookup"><span data-stu-id="151cf-135">This is necessary for writing portable code because the size of a handle varies, depending on the version of Windows.</span></span> <span data-ttu-id="151cf-136">Le cast (**uint \_ ptr**) garantit une conversion correcte.</span><span class="sxs-lookup"><span data-stu-id="151cf-136">The (**UINT\_PTR**) cast ensures proper conversion.</span></span> <span data-ttu-id="151cf-137">Le code suivant montre un exemple dans lequel **SendMessage** retourne un handle à un pinceau :</span><span class="sxs-lookup"><span data-stu-id="151cf-137">The following code shows an example in which **SendMessage** returns a handle to a brush:</span></span>


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



<span data-ttu-id="151cf-138">Les paramètres **CreateWindow** et **CreateWindowEx** *HMENU* sont parfois utilisés pour passer un identificateur de contrôle entier (ID).</span><span class="sxs-lookup"><span data-stu-id="151cf-138">The **CreateWindow** and **CreateWindowEx** parameter *hmenu* is sometimes used to pass an integer control identifier (ID).</span></span> <span data-ttu-id="151cf-139">Dans ce cas, vous devez effectuer un cast de l’ID en un type **HMENU** :</span><span class="sxs-lookup"><span data-stu-id="151cf-139">In this case, you must cast the ID to an **HMENU** type:</span></span>


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a><span data-ttu-id="151cf-140">Considérations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="151cf-140">Additional Considerations</span></span>

<span data-ttu-id="151cf-141">Pour tirer le meilleur parti de la vérification de type **stricte** , vous devez suivre des instructions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="151cf-141">To get the most benefit from **STRICT** type checking, there are additional guidelines you should follow.</span></span> <span data-ttu-id="151cf-142">Votre code sera plus portable dans les futures versions de Windows si vous apportez les modifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="151cf-142">Your code will be more portable in future versions of Windows if you make the following changes.</span></span>

<span data-ttu-id="151cf-143">Les types **wParam**, **lParam**, **LRESULT** et **LPVOID** sont des *types de données polymorphes*.</span><span class="sxs-lookup"><span data-stu-id="151cf-143">The types **WPARAM**, **LPARAM**, **LRESULT**, and **LPVOID** are *polymorphic data types*.</span></span> <span data-ttu-id="151cf-144">Ils contiennent différents genres de données à des moments différents, même si la vérification de type **stricte** est activée.</span><span class="sxs-lookup"><span data-stu-id="151cf-144">They hold different kinds of data at different times, even when **STRICT** type checking is enabled.</span></span> <span data-ttu-id="151cf-145">Pour tirer parti de la vérification de type, vous devez effectuer un cast des valeurs de ces types dès que possible.</span><span class="sxs-lookup"><span data-stu-id="151cf-145">To get the benefit of type checking, you should cast values of these types as soon as possible.</span></span> <span data-ttu-id="151cf-146">(Notez que les craqueurs de messages refont automatiquement *wParam* et *lParam* pour vous de manière portable.)</span><span class="sxs-lookup"><span data-stu-id="151cf-146">(Note that message crackers automatically recast *wParam* and *lParam* for you in a portable way.)</span></span>

<span data-ttu-id="151cf-147">Faites particulièrement attention pour distinguer les types **HMODULE** et **HINSTANCE** .</span><span class="sxs-lookup"><span data-stu-id="151cf-147">Take special care to distinguish **HMODULE** and **HINSTANCE** types.</span></span> <span data-ttu-id="151cf-148">Même si **strict** est activé, ils sont définis comme étant du même type de base.</span><span class="sxs-lookup"><span data-stu-id="151cf-148">Even with **STRICT** enabled, they are defined as the same base type.</span></span> <span data-ttu-id="151cf-149">La plupart des fonctions de gestion du module de noyau utilisent des types **HINSTANCE** , mais il existe quelques fonctions qui retournent ou acceptent uniquement des types **HMODULE** .</span><span class="sxs-lookup"><span data-stu-id="151cf-149">Most kernel module management functions use **HINSTANCE** types, but there are a few functions that return or accept only **HMODULE** types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="151cf-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="151cf-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="151cf-151">Désactivation de STRICT</span><span class="sxs-lookup"><span data-stu-id="151cf-151">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="151cf-152">Activation du STRICT</span><span class="sxs-lookup"><span data-stu-id="151cf-152">Enabling STRICT</span></span>](enabling-strict.md)
</dt> </dl>

 

 