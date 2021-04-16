---
title: URI de ressource
description: Un URI de ressource est un identificateur pour un type distinct d’opération de gestion ou de valeur utilisée par les services de gestion qui implémentent le protocole WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507930"
---
# <a name="resource-uris"></a>URI de ressource

Un [*URI de ressource*](windows-remote-management-glossary.md) est un identificateur pour un type distinct d’opération de gestion ou de valeur utilisée par les services de gestion qui implémentent le protocole WS-Management. Une valeur de gestion peut être la température à l’intérieur d’un ordinateur. Un exemple d’opération de gestion est le démarrage d’un service arrêté ou la définition d’un quota d’utilisateur de volume de disque.

## <a name="resource-uri-format"></a>Format URI de ressource

Un URI se compose d’un préfixe et d’un chemin d’accès à une ressource, comme indiqué dans l’exemple suivant :

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Cette spécification de schéma indique que l’URI est basé sur la version 1 du protocole WS-Management officiel et que la ressource est [**un \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l' \\ espace de noms « root cimv2 » de l’espace de stockage WMI. Les préfixes d’URI contiennent une spécification de schéma, telle que « schemas.microsoft.com/wbem/wsman/1/wmi » et un type spécifique de ressource, tel que **\_ disque logique Win32**. Pour plus d’informations sur l’identification d’une instance spécifique d’une classe WMI, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).

Pour plus d’informations, consultez [préfixes d’URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Types d’URI de ressource

Bien que [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) soit la principale source de données de gestion pour les systèmes d’exploitation Windows, d’autres sources de schéma de gestion existent également.

La liste suivante décrit plusieurs types d’URI de ressource utilisés par Windows Remote Management :

-   URI WMI

    Ce groupe d’URI représente un [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) chemin de classe qui comprend l’espace de noms et la classe.

    Les URI WMI peuvent être utilisés dans :

    -   Méthodes de [**session**](session.md)
    -   Méthodes [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   Méthodes [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) ou [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   Méthodes [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   URI IPMI

    Ce groupe d’URI représente des URI standard basés sur la version 2,9 de CIM. Les URI IPMI peuvent être utilisés dans les méthodes de [**session**](session.md) [**, d'**](session-put.md) [**extraction**](session-get.md), d' [**énumération**](session-enumerate.md) et d' [**appel**](session-invoke.md).

    par exemple https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Cette ressource est définie selon le schéma CIM [DMTF.org](https://www.dmtf.org/home) .

-   URI de configuration WinRM

    Ce groupe d’URI sont des opérations de configuration pour la configuration de l'[*écouteur*](windows-remote-management-glossary.md) WinRM.

    https://schemas.microsoft.com/wbem/wsman/1/config/listenerpeut être utilisé dans [](session.md) les méthodes de session [**, d'**](session-put.md) [**extraction**](session-get.md), de [**création**](session-create.md), de [**suppression**](session-delete.md)et d' [**énumération**](session-enumerate.md).

-   URI du [*Journal des événements système*](windows-remote-management-glossary.md) (sel)

    Ce groupe d’URI s’abonne aux événements du collecteur d’événements à partir du BMC. Vous pouvez vous abonner à ces événements à l’aide de l’outil en ligne de commande **wevtutil** . Pour plus d’informations, consultez https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Respect de la casse

Le [*plug-in WMI*](windows-remote-management-glossary.md) conserve la casse de l’URI de ressource reçu dans une demande. Toutefois, pour garantir l’interopérabilité avec d’autres implémentations de WS-Management protocole, utilisez la casse correcte pour la ressource demandée dans URI de ressource. La casse correcte est l’orthographe définie par le fournisseur de ressources.

Si les URI de ressource ne nécessitent pas de respect de la casse, le XML de [*fragments*](windows-remote-management-glossary.md) ne le fait pas. Un fragment spécifie une seule propriété, plutôt que l’ensemble des propriétés d’une ressource. Dans le cas des ressources WMI, la syntaxe de fragment obtient une propriété à partir d’une instance de ressource. Par exemple, l’obtention de la propriété de **version** de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requiert l’utilisation d’un fragment. Pour plus d’informations sur les fragments, consultez « Ajout d’un sélecteur à un objet ResourceLocator ou IWSManResourceLocator » dans [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).

Conformément aux normes XML et [*XPath*](windows-remote-management-glossary.md) , le [*plug-in WMI*](windows-remote-management-glossary.md) applique le respect de la casse pour les fragments et le XML qui définit les paramètres d’entrée d’une méthode. Le respect de la casse est requis pour prendre en charge la norme XPath 1.0/niveau 1. Pour recevoir des données WMI via WinRM, le respect de la casse signifie que les noms des classes, propriétés et méthodes WMI doivent correspondre à la casse du nom trouvé dans le référentiel WMI.

Pour plus d’informations, consultez [syntaxe XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Exemples de respect de la casse

Par exemple, un script qui obtient la propriété **du \_ descripteur de sécurité** à partir d’une instance de la classe de [**\_ service WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) ne peut pas utiliser les majuscules pour les noms du chemin d’accès du fragment, mais uniquement l’URI. Le [*plug-in WMI*](windows-remote-management-glossary.md) WinRM retourne une erreur pour l’exemple VBScript suivant, car le XML XPath fourni pour **FragmentPath** n’utilise pas la casse correcte. Dans le référentiel WMI, la classe est orthographiée « Win32 \_ service ».


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



La version suivante du même exemple illustre l’utilisation correcte de case pour la classe [**de \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) et la propriété de **\_ descripteur de sécurité** .


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Gestion matérielle à distance](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 