---
description: Vous pouvez utiliser les méthodes de l’objet SWbemLocator pour obtenir un objet SWbemServices qui représente une connexion à un espace de noms sur un ordinateur local ou un ordinateur hôte distant.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Objet SWbemLocator (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0e93e9bd0bfb33c495b30afbde47bcb9b007acb4cd00dece42e1a8c3b88e99d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732790"
---
# <a name="swbemlocator-object"></a>Objet SWbemLocator

Vous pouvez utiliser les méthodes de l’objet **SWbemLocator** pour obtenir un objet [**SWbemServices**](swbemservices.md) qui représente une connexion à un espace de noms sur un ordinateur local ou un ordinateur hôte distant. Vous pouvez ensuite utiliser les méthodes de l’objet **SWbemServices** pour accéder à WMI. Cet objet peut être créé par l’appel VBScript **CreateObject** .

## <a name="members"></a>Membres

L’objet **SWbemLocator** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemLocator** a ces méthodes.



| Méthode                                              | Description                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | Établit une connexion à WMI sur l’ordinateur spécifié.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemLocator** a ces propriétés.



| Propriété                                                | Type d’accès          | Description                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sécurité\_**](swbemlocator-security-.md)<br/> | Lecture seule<br/> | Utilisé pour lire ou modifier les paramètres de sécurité.<br/> |



 

## <a name="remarks"></a>Remarques

En haut du modèle d’objet de la bibliothèque de scripts WMI se trouve l’objet SWbemLocator. SWbemLocator est utilisé pour établir une connexion authentifiée à un espace de noms WMI, de la même façon que la fonction GetObject de VBScript et le moniker WMI « winmgmts : » sont utilisés pour établir une connexion authentifiée à WMI. Toutefois, SWbemLocator est conçu pour traiter deux scénarios de script spécifiques qui ne peuvent pas être exécutés à l’aide de GetObject et du moniker WMI. Vous devez utiliser SWbemLocator si vous avez besoin de :

-   Fournissez les informations d’identification de l’utilisateur et du mot de passe pour se connecter à WMI sur un ordinateur distant. Le moniker WMI utilisé avec la fonction GetObject n’inclut pas de mécanisme permettant de spécifier les informations d’identification. La plupart des activités WMI (y compris toutes celles effectuées sur des ordinateurs distants) requièrent des droits d’administrateur. Si vous vous connectez généralement à l’aide d’un compte d’utilisateur standard au lieu d’un compte d’administrateur, vous ne pourrez pas effectuer la plupart des tâches WMI, sauf si vous exécutez le script sous autres informations d’identification.
-   Connecter à WMI si vous exécutez un script wmi à partir d’une page Web. Vous ne pouvez pas utiliser la fonction GetObject lors de l’exécution de scripts incorporés dans une page HTML, car Internet Explorer interdit l’utilisation de GetObject pour des raisons de sécurité.

En outre, vous souhaiterez peut-être utiliser SWbemLocator pour vous connecter à WMI si vous trouvez la chaîne de connexion WMI utilisée avec la fonction GetObject déroutante ou difficile.

Vous utilisez CreateObject au lieu de GetObject pour créer une référence à SWbemLocator. Pour créer la référence, vous devez passer à la fonction CreateObject l’identificateur programmatique SWbemLocator (ProgID) « WbemScripting. SWbemLocator », comme indiqué sur la ligne 2 dans l’exemple de script suivant. Après avoir obtenu une référence à un objet SWbemLocator, vous appelez la méthode ConnectServer pour vous connecter à WMI et obtenir une référence à un objet SWbemServices. Cela est illustré à la ligne 3 du script suivant.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Pour exécuter un script sous d’autres informations d’identification, incluez le nom d’utilisateur et le mot de passe en tant que paramètres supplémentaires passés à ConnectServer. Par exemple, ce script s’exécute sous les informations d’identification d’un utilisateur nommé kenmyer, avec le mot de passe HomerJ.


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Vous pouvez également utiliser le \\ format de nom d’utilisateur de domaine pour spécifier un nom d’utilisateur. Par exemple :

`" fabrikam\kenmyer"`

## <a name="examples"></a>Exemples

L’exemple PowerShell suivant utilise **SWbemLocator** pour se connecter à un serveur.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




