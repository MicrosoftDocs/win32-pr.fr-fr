---
title: Inscription de l’extension de création d’objet
description: Quand une DLL d’extension de création d’objet est créée dans Active Directory Domain Services, elle doit être inscrite auprès du Registre Windows et Active Directory Domain Services pour que COM et les composants logiciels enfichables MMC d’administration Active Directory prennent en compte l’extension.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940800"
---
# <a name="registering-the-object-creation-extension"></a><span data-ttu-id="1bd1e-103">Inscription de l’extension de création d’objet</span><span class="sxs-lookup"><span data-stu-id="1bd1e-103">Registering the Object Creation Extension</span></span>

<span data-ttu-id="1bd1e-104">Quand une DLL d’extension de création d’objet est créée dans Active Directory Domain Services, elle doit être inscrite auprès du Registre Windows et Active Directory Domain Services pour que COM et les composants logiciels enfichables MMC d’administration Active Directory prennent en compte l’extension.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-104">When an object creation extension DLL in Active Directory Domain Services is created, it must be registered with the Windows registry and Active Directory Domain Services to make COM and the Active Directory administrative MMC snap-ins aware of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="1bd1e-105">Inscription dans le Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1bd1e-105">Registering in the Windows Registry</span></span>

<span data-ttu-id="1bd1e-106">Comme tous les serveurs COM, une extension de création d’objet doit être inscrite dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-106">Like all COM servers, an object creation extension must be registered in the Windows registry.</span></span> <span data-ttu-id="1bd1e-107">L’extension est inscrite sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="1bd1e-107">The extension is registered under the following key:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

<span data-ttu-id="1bd1e-108">« &lt; CLSID &gt; d’extension » est la représentation sous forme de chaîne du CLSID telle qu’elle est produite par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="1bd1e-108">"&lt;extension CLSID&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="1bd1e-109">« &lt; chemin d’accès &gt; de l’extension » contient le chemin d’accès et le nom de fichier de la dll d’extension.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-109">"&lt;extension path&gt;" contains the path and file name of the extension DLL.</span></span> <span data-ttu-id="1bd1e-110">La valeur **ThreadingModel** pour toutes les extensions de création d’objet doit être « Apartment ».</span><span class="sxs-lookup"><span data-stu-id="1bd1e-110">The **ThreadingModel** value for all object creation extensions must be "Apartment".</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="1bd1e-111">Inscription avec Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="1bd1e-111">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="1bd1e-112">L’inscription de l’extension de création d’objet est spécifique à un paramètre régional.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-112">Object creation extension registration is specific to one locale.</span></span> <span data-ttu-id="1bd1e-113">Si l’extension de création d’objet s’applique à tous les paramètres régionaux, elle doit être inscrite dans l’objet **displaySpecifier** de la classe d’objets dans tous les sous-conteneurs de paramètres régionaux du conteneur DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-113">If the object creation extension applies to all locales, it must be registered in the object class's **displaySpecifier** object in all of the locale subcontainers in the DisplaySpecifiers container.</span></span> <span data-ttu-id="1bd1e-114">Si l’extension de création d’objet est localisée pour certains paramètres régionaux, inscrivez-la dans l’objet **displaySpecifier** dans le sous-conteneur de ces paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-114">If the object creation extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="1bd1e-115">Pour plus d’informations sur le conteneur DisplaySpecifiers et les paramètres régionaux, consultez [spécificateurs d’affichage](display-specifiers.md) et [conteneur DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1e-115">For more information about the DisplaySpecifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="1bd1e-116">Il existe deux attributs DisplaySpecifier sous lesquels une extension de création d’objet peut être inscrite.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-116">There are two DisplaySpecifier attributes that an object creation extension can be registered under.</span></span> <span data-ttu-id="1bd1e-117">Il s’agit de **creationWizard** et **createWizardExt**.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-117">These are **creationWizard** and **createWizardExt**.</span></span>

<span data-ttu-id="1bd1e-118">L’attribut **creationWizard** identifie les extensions de création d’objet principal pour remplacer l’Assistant Création d’objet existant ou natif dans Active Directory composants logiciels enfichables d’administration. Une extension de création principale fournit le premier ensemble de pages et est hébergée de la même façon que les pages natives.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-118">The **creationWizard** attribute identifies primary object creation extensions to replace the existing or native object creation wizard in Active Directory administrative snap-ins. A primary creation extension provides the first set of pages and is hosted in the same way as native pages.</span></span> <span data-ttu-id="1bd1e-119">Cet attribut est à valeur unique et requiert le format suivant :</span><span class="sxs-lookup"><span data-stu-id="1bd1e-119">This attribute is single-valued and requires the following format:</span></span>


```C++
<CLSID>
```



<span data-ttu-id="1bd1e-120">Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID de l’objet com, tel qu’il est généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="1bd1e-120">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="1bd1e-121">L’attribut **createWizardExt** identifie les extensions de création d’objets secondaires.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-121">The **createWizardExt** attribute identifies secondary object creation extensions.</span></span> <span data-ttu-id="1bd1e-122">Une extension de création secondaire ajoute des pages d’assistant aux pages natives ou à l’extension principale.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-122">A secondary creation extension adds wizard pages to the native pages or primary extension.</span></span> <span data-ttu-id="1bd1e-123">Cet attribut est à valeurs multiples et requiert le format suivant :</span><span class="sxs-lookup"><span data-stu-id="1bd1e-123">This attribute is multi-valued and requires the following format:</span></span>


```C++
<order number>,<CLSID>
```



<span data-ttu-id="1bd1e-124">« &lt; Order Number &gt; » est un nombre non signé qui représente la position de la page dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-124">The "&lt;order number&gt;" is an unsigned number that represents the page's position in the wizard.</span></span> <span data-ttu-id="1bd1e-125">Quand un assistant de création est affiché, les valeurs sont triées à l’aide d’une comparaison entre le « numéro d’ordre » de chaque valeur &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="1bd1e-125">When a creation wizard is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="1bd1e-126">Si plusieurs valeurs ont le même « numéro de &lt; commande &gt; », ces pages sont chargées dans l’ordre dans lequel elles sont lues à partir du serveur de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-126">If more than one value has the same "&lt;order number&gt;", those pages are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="1bd1e-127">Si possible, vous devez utiliser un « &lt; numéro d’ordre » non existant &gt; (autrement dit, un numéro qui n’a pas été utilisé par d’autres valeurs de la propriété).</span><span class="sxs-lookup"><span data-stu-id="1bd1e-127">If possible, you should use a non-existing "&lt;order number&gt;" (that is, one that has not been used by other values in the property).</span></span> <span data-ttu-id="1bd1e-128">Il n’y a pas de position de départ prescrite, et les espaces sont autorisés dans la &lt; séquence « Order Number &gt; ».</span><span class="sxs-lookup"><span data-stu-id="1bd1e-128">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="1bd1e-129">Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID de l’objet com, tel qu’il est généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="1bd1e-129">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

 

 