---
title: Inscription de l’objet COM de la page de propriétés dans un spécificateur d’affichage
description: Cette rubrique montre comment inscrire une DLL d’extension qui contient une feuille de propriétés Active Directory avec le Registre Windows et Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Inscription de l’objet COM de la page de propriétés dans un spécificateur d’affichage Active Directory
- Active Directory d’objets COM de page de propriétés, inscription dans un spécificateur d’affichage
- spécificateurs d’affichage Active Directory, inscription de l’objet COM page de propriétés dans
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5b08ac0ea6329026a6d367e71064bde917b1a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101428"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a><span data-ttu-id="bb33f-106">Inscription de l’objet COM de la page de propriétés dans un spécificateur d’affichage</span><span class="sxs-lookup"><span data-stu-id="bb33f-106">Registering the Property Page COM Object in a Display Specifier</span></span>

<span data-ttu-id="bb33f-107">Lorsque vous utilisez COM pour créer une DLL d’extension de feuille de propriétés pour Active Directory Domain Services, vous devez également enregistrer l’extension avec le Registre Windows et Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="bb33f-107">When you use COM to create a property sheet extension DLL for Active Directory Domain Services, you must also register the extension with the Windows registry and Active Directory Domain Services.</span></span> <span data-ttu-id="bb33f-108">L’inscription de l’extension permet au Active Directory composants logiciels enfichables MMC d’administration et au shell Windows de reconnaître l’extension.</span><span class="sxs-lookup"><span data-stu-id="bb33f-108">Registering the extension enables the Active Directory administrative MMC snap-ins and the Windows shell to recognize the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="bb33f-109">Inscription dans le Registre Windows</span><span class="sxs-lookup"><span data-stu-id="bb33f-109">Registering in the Windows Registry</span></span>

<span data-ttu-id="bb33f-110">Comme tous les serveurs COM, une extension de feuille de propriétés doit être inscrite dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="bb33f-110">Like all COM servers, a property sheet extension must be registered in the Windows registry.</span></span> <span data-ttu-id="bb33f-111">L’extension est inscrite sous la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="bb33f-111">The extension is registered under the following key.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

<span data-ttu-id="bb33f-112">*<clsid>* représentation sous forme de chaîne du CLSID telle qu’elle est produite par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="bb33f-112">*<clsid>* is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="bb33f-113">Sous la *<clsid>* clé, il existe une clé **InprocServer32** qui identifie l’objet en tant que serveur in-proc 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bb33f-113">Under the *<clsid>* key, there is an **InProcServer32** key that identifies the object as a 32-bit in-proc server.</span></span> <span data-ttu-id="bb33f-114">Sous la clé **InprocServer32** , l’emplacement de la dll est spécifié dans la valeur par défaut et le modèle de thread est spécifié dans la valeur **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="bb33f-114">Under the **InProcServer32** key, the location of the DLL is specified in the default value and the threading model is specified in the **ThreadingModel** value.</span></span> <span data-ttu-id="bb33f-115">Toutes les extensions de feuille de propriétés doivent utiliser le modèle de thread « Apartment ».</span><span class="sxs-lookup"><span data-stu-id="bb33f-115">All property sheet extensions must use the "Apartment" threading model.</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="bb33f-116">Inscription avec Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="bb33f-116">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="bb33f-117">L’inscription de l’extension de la feuille de propriétés est spécifique à un paramètre régional.</span><span class="sxs-lookup"><span data-stu-id="bb33f-117">Property sheet extension registration is specific to one locale.</span></span> <span data-ttu-id="bb33f-118">Si l’extension de la feuille de propriétés s’applique à tous les paramètres régionaux, elle doit être inscrite dans l’objet [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la classe d’objet dans tous les sous-conteneurs de paramètres régionaux dans le conteneur de spécificateurs d’affichage.</span><span class="sxs-lookup"><span data-stu-id="bb33f-118">If the property sheet extension applies to all locales, it must be registered in the object class [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) object in all of the locale subcontainers in the Display Specifiers container.</span></span> <span data-ttu-id="bb33f-119">Si l’extension de la feuille de propriétés est localisée pour un certain nombre de paramètres régionaux, inscrivez-la dans l’objet **displaySpecifier** de ce sous-conteneur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="bb33f-119">If the property sheet extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale subcontainer.</span></span> <span data-ttu-id="bb33f-120">Pour plus d’informations sur le conteneur et les paramètres régionaux des spécificateurs d’affichage, consultez [spécificateurs d’affichage](display-specifiers.md) et [conteneur DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="bb33f-120">For more information about the Display Specifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="bb33f-121">Il existe trois attributs de spécificateur d’affichage sous lesquels une extension de feuille de propriétés peut être inscrite.</span><span class="sxs-lookup"><span data-stu-id="bb33f-121">There are three display specifier attributes that a property sheet extension can be registered under.</span></span> <span data-ttu-id="bb33f-122">Il s’agit des [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)et [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span><span class="sxs-lookup"><span data-stu-id="bb33f-122">These are [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), and [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span></span>

<span data-ttu-id="bb33f-123">L’attribut [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifie les pages de propriétés d’administration à afficher dans Active Directory composants logiciels enfichables d’administration. La page de propriétés s’affiche lorsque l’utilisateur consulte les propriétés des objets de la classe appropriée dans l’un des composants logiciels enfichables MMC d’administration de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bb33f-123">The [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) attribute identifies administrative property pages to display in Active Directory administrative snap-ins. The property page appears when the user views properties for objects of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="bb33f-124">L’attribut [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) identifie les pages de propriétés de l’utilisateur final à afficher dans le shell Windows.</span><span class="sxs-lookup"><span data-stu-id="bb33f-124">The [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attribute identifies end-user property pages to display in the Windows shell.</span></span> <span data-ttu-id="bb33f-125">La page de propriétés s’affiche lorsque l’utilisateur consulte les propriétés des objets de la classe appropriée dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="bb33f-125">The property page appears when the user views the properties for objects of the appropriate class in the Windows Explorer.</span></span> <span data-ttu-id="bb33f-126">Depuis les systèmes d’exploitation Windows Server 2003, l’interpréteur de commandes Windows n’affiche plus d’objets de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="bb33f-126">Beginning with the Windows Server 2003 operating systems, the Windows shell no longer displays objects from Active Directory Domain Services.</span></span>

<span data-ttu-id="bb33f-127">Le [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) est disponible uniquement sur les systèmes d’exploitation Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb33f-127">The [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) is only available on the Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bb33f-128">La page de propriétés s’affiche lorsque l’utilisateur consulte les propriétés de plusieurs objets de la classe appropriée dans l’un des composants logiciels enfichables MMC d’administration de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bb33f-128">The property page appears when the user views properties for more than one object of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="bb33f-129">Tous ces attributs sont à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="bb33f-129">All of these attributes are multi-valued.</span></span>

<span data-ttu-id="bb33f-130">Les valeurs des attributs [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) et [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) requièrent le format suivant.</span><span class="sxs-lookup"><span data-stu-id="bb33f-130">The values for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) and [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attributes require the following format.</span></span>


```C++
<order number>,<clsid>,<optional data>
```



<span data-ttu-id="bb33f-131">Les valeurs de l’attribut [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) nécessitent le format suivant.</span><span class="sxs-lookup"><span data-stu-id="bb33f-131">The values for the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute require the following format.</span></span>


```C++
<order number>,<clsid>
```



<span data-ttu-id="bb33f-132">« &lt; Order Number &gt; » est un nombre non signé qui représente la position de la page dans la feuille.</span><span class="sxs-lookup"><span data-stu-id="bb33f-132">The "&lt;order number&gt;" is an unsigned number that represents the page position in the sheet.</span></span> <span data-ttu-id="bb33f-133">Lorsqu’une feuille de propriétés est affichée, les valeurs sont triées à l’aide d’une comparaison du « numéro d’ordre » de chaque valeur &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="bb33f-133">When a property sheet is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="bb33f-134">Si plusieurs valeurs ont le même « numéro de &lt; commande &gt; », ces objets COM de page de propriétés sont chargés dans l’ordre dans lequel ils sont lus à partir du serveur de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bb33f-134">If more than one value has the same "&lt;order number&gt;", those property page COM objects are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="bb33f-135">Si possible, vous devez utiliser un « &lt; numéro d’ordre » non existant &gt; ; autrement dit, il n’est pas utilisé par d’autres valeurs de la propriété.</span><span class="sxs-lookup"><span data-stu-id="bb33f-135">If possible, you should use a non-existing "&lt;order number&gt;"; that is, one not used by other values in the property.</span></span> <span data-ttu-id="bb33f-136">Il n’y a pas de position de départ prescrite, et les espaces sont autorisés dans la &lt; séquence « Order Number &gt; ».</span><span class="sxs-lookup"><span data-stu-id="bb33f-136">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="bb33f-137">Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID tel qu’il a été généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="bb33f-137">The "&lt;clsid&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="bb33f-138">« &lt; Données facultatives &gt; » est une valeur de chaîne qui n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bb33f-138">The "&lt;optional data&gt;" is a string value that is not required.</span></span> <span data-ttu-id="bb33f-139">Cette valeur peut être récupérée par l’objet COM page de propriétés à l’aide du pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passé à sa méthode [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="bb33f-139">This value can be retrieved by the property page COM object using the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to its [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method.</span></span> <span data-ttu-id="bb33f-140">L’objet COM page de propriétés obtient ces données en appelant [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) avec le format de presse-papiers [**CFSTR \_ DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="bb33f-140">The property page COM object obtains this data by calling [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) with the [**CFSTR\_DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) clipboard format.</span></span> <span data-ttu-id="bb33f-141">Cela fournit un **HGLOBAL** qui contient une structure [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) la structure **DSPROPERTYPAGEINFO** contient une chaîne Unicode qui contient les « &lt; données facultatives &gt; ».</span><span class="sxs-lookup"><span data-stu-id="bb33f-141">This provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure The **DSPROPERTYPAGEINFO** structure contains a Unicode string that contains the "&lt;optional data&gt;".</span></span> <span data-ttu-id="bb33f-142">Les « &lt; données facultatives &gt; » ne sont pas autorisées avec l’attribut [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .</span><span class="sxs-lookup"><span data-stu-id="bb33f-142">The "&lt;optional data&gt;" is not allowed with the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute.</span></span> <span data-ttu-id="bb33f-143">L’exemple de code C/C++ suivant montre comment récupérer les « &lt; données facultatives &gt; ».</span><span class="sxs-lookup"><span data-stu-id="bb33f-143">The following C/C++ code example shows how to retrieve the "&lt;optional data&gt;".</span></span>


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



<span data-ttu-id="bb33f-144">Une extension de feuille de propriétés peut implémenter plusieurs pages de propriétés ; une utilisation possible des « &lt; données facultatives &gt; » consiste à nommer les pages à afficher.</span><span class="sxs-lookup"><span data-stu-id="bb33f-144">A property sheet extension can implement more than one property page; one possible use of the "&lt;optional data&gt;" is to name the pages to display.</span></span> <span data-ttu-id="bb33f-145">Cela offre la possibilité de choisir d’implémenter plusieurs objets COM, un pour chaque page ou un objet COM unique pour gérer plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="bb33f-145">This provides the flexibility of choosing to implement multiple COM objects, one for each page, or a single COM object to handle multiple pages.</span></span>

<span data-ttu-id="bb33f-146">L’exemple de code suivant est une valeur d’exemple qui peut être utilisée pour les attributs [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)ou [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .</span><span class="sxs-lookup"><span data-stu-id="bb33f-146">The following code example is an example value that can be used for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), or [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attributes.</span></span>


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> <span data-ttu-id="bb33f-147">Pour le shell Windows, les données du spécificateur d’affichage sont récupérées à l’ouverture de session de l’utilisateur et mises en cache pour la session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb33f-147">For the Windows shell, display specifier data is retrieved at user logon, and cached for the user session.</span></span> <span data-ttu-id="bb33f-148">Pour les composants logiciels enfichables d’administration, les données du spécificateur d’affichage sont récupérées lorsque le composant logiciel enfichable est chargé et sont mises en cache pour la durée de vie du processus.</span><span class="sxs-lookup"><span data-stu-id="bb33f-148">For administrative snap-ins, the display specifier data is retrieved when the snap-in is loaded, and is cached for the lifetime of the process.</span></span> <span data-ttu-id="bb33f-149">Pour le shell Windows, cela indique que les modifications apportées aux spécificateurs d’affichage prennent effet après qu’un utilisateur se déconnecte, puis se reconnecte.</span><span class="sxs-lookup"><span data-stu-id="bb33f-149">For the Windows shell, this indicates that changes to display specifiers take effect after a user logs off and then logs on again.</span></span> <span data-ttu-id="bb33f-150">Pour les composants logiciels enfichables d’administration, les modifications prennent effet lors du chargement du composant logiciel enfichable ou de la console.</span><span class="sxs-lookup"><span data-stu-id="bb33f-150">For the administrative snap-ins, changes take effect when the snap-in or console file is loaded.</span></span>

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a><span data-ttu-id="bb33f-151">Ajout d’une valeur aux attributs d’extension de la feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="bb33f-151">Adding a Value to the Property Sheet Extension Attributes</span></span>

<span data-ttu-id="bb33f-152">La procédure suivante décrit comment inscrire une extension de feuille de propriétés sous l’un des attributs d’extension de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bb33f-152">The following procedure describes how to register a property sheet extension under one of the property sheet extension attributes.</span></span>

<span data-ttu-id="bb33f-153">**Inscription d’une extension de feuille de propriétés sous l’un des attributs d’extension de la feuille de propriétés**</span><span class="sxs-lookup"><span data-stu-id="bb33f-153">**Registering a property sheet extension under one of the property sheet extension attributes**</span></span>

1.  <span data-ttu-id="bb33f-154">Assurez-vous que l’extension n’existe pas déjà dans les valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="bb33f-154">Ensure that the extension does not already exist in the attribute values.</span></span>
2.  <span data-ttu-id="bb33f-155">Ajoutez la nouvelle valeur à la fin de la liste classement des pages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bb33f-155">Add the new value at the end of the property page ordering list.</span></span> <span data-ttu-id="bb33f-156">Cela permet de définir la &lt; partie « Order Number &gt; » de la valeur de l’attribut sur la valeur suivante après le numéro de commande existant le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="bb33f-156">That is set the "&lt;order number&gt;" portion of the attribute value to the next value after the highest existing order number.</span></span>
3.  <span data-ttu-id="bb33f-157">La méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) est utilisée pour ajouter la nouvelle valeur à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="bb33f-157">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="bb33f-158">Le paramètre *lnControlCode* doit être défini sur **la \_ propriété \_ Append de publicité** afin que la nouvelle valeur soit ajoutée aux valeurs existantes et ne remplace donc pas les valeurs existantes.</span><span class="sxs-lookup"><span data-stu-id="bb33f-158">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND** so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="bb33f-159">La méthode [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) doit être appelée par la suite pour valider la modification dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="bb33f-159">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called afterward to commit the change to the directory.</span></span>

<span data-ttu-id="bb33f-160">Sachez que la même extension de feuille de propriétés peut être inscrite pour plusieurs classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="bb33f-160">Be aware that the same property sheet extension can be registered for more than one object class.</span></span>

<span data-ttu-id="bb33f-161">La méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) est utilisée pour ajouter la nouvelle valeur à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="bb33f-161">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="bb33f-162">Le paramètre *lnControlCode* doit être défini sur **la \_ propriété \_ Append de publicités**, afin que la nouvelle valeur soit ajoutée aux valeurs existantes et ne remplace pas les valeurs existantes.</span><span class="sxs-lookup"><span data-stu-id="bb33f-162">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND**, so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="bb33f-163">La méthode [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) doit être appelée après pour valider la modification dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="bb33f-163">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called after to commit the change to the directory.</span></span>

<span data-ttu-id="bb33f-164">L’exemple de code suivant ajoute une extension de feuille de propriétés à la classe de groupe dans les paramètres régionaux par défaut de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bb33f-164">The following code example adds a property sheet extension to the group class in the computer's default locale.</span></span> <span data-ttu-id="bb33f-165">N’oubliez pas que la fonction **AddPropertyPageToDisplaySpecifier** vérifie le CLSID de l’extension de la feuille de propriétés dans les valeurs existantes, obtient le numéro d’ordre le plus élevé et ajoute la valeur de la page de propriétés à l’aide de [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec la **\_ propriété ADS \_ Ajouter** le code de contrôle.</span><span class="sxs-lookup"><span data-stu-id="bb33f-165">Be aware that the **AddPropertyPageToDisplaySpecifier** function verifies the property sheet extension CLSID in the existing values, gets the highest order number, and adds the value for the property page using [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) with the **ADS\_PROPERTY\_APPEND** control code.</span></span>


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 