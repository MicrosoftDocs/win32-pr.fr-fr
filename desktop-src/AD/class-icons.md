---
title: Icônes de classe
description: L’icône utilisée pour représenter un objet de classe peut être spécifiée dans l’attribut iconPath du conteneur DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- noms d’affichage de classes Active Directory, icônes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940838"
---
# <a name="class-icons"></a><span data-ttu-id="c06f3-104">Icônes de classe</span><span class="sxs-lookup"><span data-stu-id="c06f3-104">Class Icons</span></span>

<span data-ttu-id="c06f3-105">L’icône utilisée pour représenter un objet de classe peut être spécifiée dans l’attribut **iconPath** du conteneur DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="c06f3-105">The icon used to represent a class object can be specified in the **iconPath** attribute in the DisplaySpecifiers container.</span></span> <span data-ttu-id="c06f3-106">En outre, chaque classe peut stocker plusieurs États d’icône.</span><span class="sxs-lookup"><span data-stu-id="c06f3-106">Moreover, each class can store multiple icon states.</span></span> <span data-ttu-id="c06f3-107">Par exemple, une classe de dossiers peut avoir des icônes pour les États Open, Closed et Disabled.</span><span class="sxs-lookup"><span data-stu-id="c06f3-107">For example, a folder class can have icons for the open, closed, and disabled states.</span></span> <span data-ttu-id="c06f3-108">L’implémentation actuelle accepte un maximum de seize États d’icône différents par classe.</span><span class="sxs-lookup"><span data-stu-id="c06f3-108">The current implementation accepts a maximum of sixteen different icon states per class.</span></span>

<span data-ttu-id="c06f3-109">L’attribut **iconPath** peut être spécifié de deux façons.</span><span class="sxs-lookup"><span data-stu-id="c06f3-109">The **iconPath** attribute can be specified in one of two ways.</span></span>


```C++
<state>,<icon file name>
```



<span data-ttu-id="c06f3-110">ou</span><span class="sxs-lookup"><span data-stu-id="c06f3-110">or</span></span>


```C++
<state>,<module file name>,<resource ID>
```



<span data-ttu-id="c06f3-111">Dans ces exemples, « &lt; State &gt; » est un entier dont la valeur est comprise entre 0 et 15.</span><span class="sxs-lookup"><span data-stu-id="c06f3-111">In these examples, the "&lt;state&gt;" is an integer with a value between 0 and 15.</span></span> <span data-ttu-id="c06f3-112">La valeur 0 est définie comme étant l’État par défaut ou fermé de l’icône.</span><span class="sxs-lookup"><span data-stu-id="c06f3-112">The value 0 is defined to be the default or closed state of the icon.</span></span> <span data-ttu-id="c06f3-113">La valeur 1 est définie pour être l’état ouvert de l’icône.</span><span class="sxs-lookup"><span data-stu-id="c06f3-113">The value 1 is defined to be the open state of the icon.</span></span> <span data-ttu-id="c06f3-114">La valeur 2 est l’état désactivé.</span><span class="sxs-lookup"><span data-stu-id="c06f3-114">The value 2 is the disabled state.</span></span> <span data-ttu-id="c06f3-115">Toutes les autres valeurs sont définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="c06f3-115">All other values are application-defined.</span></span>

<span data-ttu-id="c06f3-116">« &lt; Icon File name &gt; » est le chemin d’accès et le nom de fichier d’un fichier d’icône qui contient l’image d’icône.</span><span class="sxs-lookup"><span data-stu-id="c06f3-116">The "&lt;icon file name&gt;" is the path and file name of an icon file that contains the icon image.</span></span>

<span data-ttu-id="c06f3-117">Le « &lt; nom de fichier du module &gt; » est le chemin d’accès et le nom de fichier d’un module, tel qu’un exe ou une dll, qui contient l’image d’icône dans une ressource.</span><span class="sxs-lookup"><span data-stu-id="c06f3-117">The "&lt;module file name&gt;" is the path and file name of a module, such as an EXE or DLL, that contains the icon image in a resource.</span></span> <span data-ttu-id="c06f3-118">L' &lt; ID de ressource &gt; est un entier qui spécifie l’identificateur de ressource de la ressource icône dans le module.</span><span class="sxs-lookup"><span data-stu-id="c06f3-118">The "&lt;resource ID&gt;" is an integer that specifies the resource identifier of the icon resource within the module.</span></span>

## <a name="adding-a-value-to-the-iconpath-attribute"></a><span data-ttu-id="c06f3-119">Ajout d’une valeur à l’attribut **iconPath**</span><span class="sxs-lookup"><span data-stu-id="c06f3-119">Adding a Value to the **iconPath** Attribute</span></span>

<span data-ttu-id="c06f3-120">Pour ajouter une valeur à l’attribut **iconPath** , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="c06f3-120">To add a value to the **iconPath** attribute, perform the following steps.</span></span>

1.  <span data-ttu-id="c06f3-121">Déterminez si la valeur de l’attribut existe.</span><span class="sxs-lookup"><span data-stu-id="c06f3-121">Determine if the value for the attribute exists.</span></span> <span data-ttu-id="c06f3-122">Si une valeur doit être remplacée, supprimez d’abord la valeur existante à l’aide de la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec le paramètre *LnControlCode* défini sur **ADS \_ propriété \_ Delete** et le paramètre *vProp* défini sur la valeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c06f3-122">If a value is to be replaced, first, delete the existing value using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="c06f3-123">N’utilisez pas **les \_ Propriétés ad \_ Clear** ou **ADS \_ Property \_ Update** pour *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="c06f3-123">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="c06f3-124">Créez la chaîne qui représente les données de l’icône d’attribut.</span><span class="sxs-lookup"><span data-stu-id="c06f3-124">Create the string that represents the attribute icon data.</span></span> <span data-ttu-id="c06f3-125">Pour obtenir un exemple, consultez le format ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c06f3-125">For an example, see the format above.</span></span>
3.  <span data-ttu-id="c06f3-126">Pour ajouter la nouvelle valeur, utilisez la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec le paramètre *LnControlCode* défini sur **ADS \_ propriété \_ Append**.</span><span class="sxs-lookup"><span data-stu-id="c06f3-126">To add the new value, use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND**.</span></span>
4.  <span data-ttu-id="c06f3-127">Pour valider les modifications apportées à l’annuaire, appelez [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="c06f3-127">To commit changes to the directory, call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 