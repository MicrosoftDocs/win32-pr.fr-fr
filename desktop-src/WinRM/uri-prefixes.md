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
# <a name="uri-prefixes"></a>Préfixes d’URI

Le préfixe [*URI de ressource*](windows-remote-management-glossary.md) diffère selon le schéma XML qui décrit la ressource.

## <a name="prefixes"></a>Préfixes

Si vous accédez à une classe [*cim*](windows-remote-management-glossary.md) 2,1, par exemple un [**fichier de \_ fichier CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), le préfixe de l’URI diffère du préfixe d’une classe CIM 2,9, par exemple **CIM \_ AdminDomain**. Les classes CIM 2,1 sont documentées dans la section des [classes CIM](/windows/desktop/WmiSdk/cimclas) de Windows Management Instrumentation (WMI).

La plupart des [classes WMI](/windows/desktop/WmiSdk/wmi-classes) se trouvent dans l’espace de noms WMI **\\ cimv2 racine** . Les classes pour le fournisseur de l’interface de gestion de plateforme intelligente ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) Microsoft se trouvent dans le **\\ matériel racine**.

La liste suivante contient les préfixes d’URI de ressource pour les schémas suivants :

-   Classes WMI ou CIM 2,1 dans l’espace de noms **\\ cimv2 racine**

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   Classes CIM 2,9 ou classes IPMI

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Autre méthode d’accès aux classes de fournisseur IPMI

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Pour plus d’informations, consultez [URI de ressource](resource-uris.md) et [chaînes URLPrefix](/windows/desktop/Http/urlprefix-strings). Pour plus d’informations sur la génération d’un URI pour une méthode ou une classe WMI, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).

## <a name="prefix-aliases"></a>Alias de préfixe

Un alias de préfixe est un raccourci qui représente le préfixe URI de ressource long. Vous pouvez également utiliser des alias dans la ligne de commande **WinRM** . Pour afficher la liste des alias disponibles, tapez **WinRM Help aliases**.

N’oubliez pas qu’un alias ne peut pas être utilisé dans une référence de point de terminaison (EPR) lors de la spécification d’un URI de ressource. Windows Remote Management ne peut pas développer l’alias lorsqu’il est incorporé en XML.

Dans l’exemple de code suivant, l’alias WinRM est utilisé dans un EPR à la place de l’URI de ressource complet, qui est `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . Dans ce cas, WinRM retourne une erreur qui indique que le service ne peut pas traiter la demande.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



La liste suivante répertorie les alias et les URI de ressource pour lesquels elles se substituent.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>WMIC
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>cimv2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>WinRM
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>WSMan
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>Shell
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Windows Remote Management et WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[URI de ressource](resource-uris.md)
</dt> </dl>
