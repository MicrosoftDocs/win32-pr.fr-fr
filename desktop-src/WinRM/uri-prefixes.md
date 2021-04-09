---
title: Préfixes d’URI
description: Le préfixe URI de ressource diffère selon le schéma XML qui décrit la ressource.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103842861"
---
# <a name="uri-prefixes"></a><span data-ttu-id="7fd1d-103">Préfixes d’URI</span><span class="sxs-lookup"><span data-stu-id="7fd1d-103">URI prefixes</span></span>

<span data-ttu-id="7fd1d-104">Le préfixe [*URI de ressource*](windows-remote-management-glossary.md) diffère selon le schéma XML qui décrit la ressource.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-104">The [*resource URI*](windows-remote-management-glossary.md) prefix is different depending on which XML schema describes the resource.</span></span>

## <a name="prefixes"></a><span data-ttu-id="7fd1d-105">Préfixes</span><span class="sxs-lookup"><span data-stu-id="7fd1d-105">Prefixes</span></span>

<span data-ttu-id="7fd1d-106">Si vous accédez à une classe [*cim*](windows-remote-management-glossary.md) 2,1, par exemple un [**fichier de \_ fichier CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), le préfixe de l’URI diffère du préfixe d’une classe CIM 2,9, par exemple **CIM \_ AdminDomain**.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-106">If you access a [*CIM*](windows-remote-management-glossary.md) 2.1 class, such as [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), the prefix of the URI differs from the prefix for a CIM 2.9 class, such as **CIM\_AdminDomain**.</span></span> <span data-ttu-id="7fd1d-107">Les classes CIM 2,1 sont documentées dans la section des [classes CIM](/windows/desktop/WmiSdk/cimclas) de Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7fd1d-107">CIM 2.1 classes are documented in the [CIM Classes](/windows/desktop/WmiSdk/cimclas) section of Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="7fd1d-108">La plupart des [classes WMI](/windows/desktop/WmiSdk/wmi-classes) se trouvent dans l’espace de noms WMI **\\ cimv2 racine** .</span><span class="sxs-lookup"><span data-stu-id="7fd1d-108">Most [WMI classes](/windows/desktop/WmiSdk/wmi-classes) are in the **root\\cimv2** WMI namespace.</span></span> <span data-ttu-id="7fd1d-109">Les classes pour le fournisseur de l’interface de gestion de plateforme intelligente ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) Microsoft se trouvent dans le **\\ matériel racine**.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-109">Classes for the Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) provider are in **root\\hardware**.</span></span>

<span data-ttu-id="7fd1d-110">La liste suivante contient les préfixes d’URI de ressource pour les schémas suivants :</span><span class="sxs-lookup"><span data-stu-id="7fd1d-110">The following list contains the resource URI prefixes for these schemas:</span></span>

-   <span data-ttu-id="7fd1d-111">Classes WMI ou CIM 2,1 dans l’espace de noms **\\ cimv2 racine**</span><span class="sxs-lookup"><span data-stu-id="7fd1d-111">WMI or CIM 2.1 classes in the **root\\cimv2** namespace</span></span>

    <span data-ttu-id="7fd1d-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span><span class="sxs-lookup"><span data-stu-id="7fd1d-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span></span>

-   <span data-ttu-id="7fd1d-113">Classes CIM 2,9 ou classes IPMI</span><span class="sxs-lookup"><span data-stu-id="7fd1d-113">CIM 2.9 classes or IPMI classes</span></span>

    <span data-ttu-id="7fd1d-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span><span class="sxs-lookup"><span data-stu-id="7fd1d-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span></span>

-   <span data-ttu-id="7fd1d-115">Autre méthode d’accès aux classes de fournisseur IPMI</span><span class="sxs-lookup"><span data-stu-id="7fd1d-115">Alternate way to access IPMI provider classes</span></span>

    <span data-ttu-id="7fd1d-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span><span class="sxs-lookup"><span data-stu-id="7fd1d-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span></span>

<span data-ttu-id="7fd1d-117">Pour plus d’informations, consultez [URI de ressource](resource-uris.md) et [chaînes URLPrefix](/windows/desktop/Http/urlprefix-strings).</span><span class="sxs-lookup"><span data-stu-id="7fd1d-117">For more information, see [Resource URIs](resource-uris.md) and [UrlPrefix Strings](/windows/desktop/Http/urlprefix-strings).</span></span> <span data-ttu-id="7fd1d-118">Pour plus d’informations sur la génération d’un URI pour une méthode ou une classe WMI, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7fd1d-118">For more information about generating a URI for a WMI class or method, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="prefix-aliases"></a><span data-ttu-id="7fd1d-119">Alias de préfixe</span><span class="sxs-lookup"><span data-stu-id="7fd1d-119">Prefix Aliases</span></span>

<span data-ttu-id="7fd1d-120">Un alias de préfixe est un raccourci qui représente le préfixe URI de ressource long.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-120">A prefix alias is a shortcut that represents the long resource URI prefix.</span></span> <span data-ttu-id="7fd1d-121">Vous pouvez également utiliser des alias dans la ligne de commande **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="7fd1d-121">You can also use aliases in the **Winrm** command-line.</span></span> <span data-ttu-id="7fd1d-122">Pour afficher la liste des alias disponibles, tapez **WinRM Help aliases**.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-122">To view a list of available aliases, type **Winrm help aliases**.</span></span>

<span data-ttu-id="7fd1d-123">N’oubliez pas qu’un alias ne peut pas être utilisé dans une référence de point de terminaison (EPR) lors de la spécification d’un URI de ressource.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-123">Be aware that an alias cannot be used inside an endpoint reference (EPR) when specifying a resource URI.</span></span> <span data-ttu-id="7fd1d-124">Windows Remote Management ne peut pas développer l’alias lorsqu’il est incorporé en XML.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-124">Windows Remote Management is unable to expand the alias when it is embedded in XML.</span></span>

<span data-ttu-id="7fd1d-125">Dans l’exemple de code suivant, l’alias WinRM est utilisé dans un EPR à la place de l’URI de ressource complet, qui est `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` .</span><span class="sxs-lookup"><span data-stu-id="7fd1d-125">In the following code example, the winrm alias is used in an EPR instead of the complete resource URI, which is `http://schemas.microsoft.com/wbem/wsman/1/config/Listener`.</span></span> <span data-ttu-id="7fd1d-126">Dans ce cas, WinRM retourne une erreur qui indique que le service ne peut pas traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-126">In this case, WinRM returns an error that indicates the service cannot process the request.</span></span>


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



<span data-ttu-id="7fd1d-127">La liste suivante répertorie les alias et les URI de ressource pour lesquels elles se substituent.</span><span class="sxs-lookup"><span data-stu-id="7fd1d-127">The following lists defined aliases and resource URIs for which they substitute.</span></span>

<dl> <dt>

<span data-ttu-id="7fd1d-128"><span id="wmi"></span><span id="WMI"></span>WMIC</span><span class="sxs-lookup"><span data-stu-id="7fd1d-128"><span id="wmi"></span><span id="WMI"></span>wmi</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span data-ttu-id="7fd1d-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span><span class="sxs-lookup"><span data-stu-id="7fd1d-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span data-ttu-id="7fd1d-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span><span class="sxs-lookup"><span data-stu-id="7fd1d-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span></span>
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span data-ttu-id="7fd1d-131"><span id="winrm"></span><span id="WINRM"></span>WinRM</span><span class="sxs-lookup"><span data-stu-id="7fd1d-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="7fd1d-132"><span id="wsman"></span><span id="WSMAN"></span>WSMan</span><span class="sxs-lookup"><span data-stu-id="7fd1d-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="7fd1d-133"><span id="shell"></span><span id="SHELL"></span>Shell</span><span class="sxs-lookup"><span data-stu-id="7fd1d-133"><span id="shell"></span><span id="SHELL"></span>shell</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7fd1d-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7fd1d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fd1d-135">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="7fd1d-135">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="7fd1d-136">Windows Remote Management et WMI</span><span class="sxs-lookup"><span data-stu-id="7fd1d-136">Windows Remote Management and WMI</span></span>](windows-remote-management-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="7fd1d-137">URI de ressource</span><span class="sxs-lookup"><span data-stu-id="7fd1d-137">Resource URIs</span></span>](resource-uris.md)
</dt> </dl>
