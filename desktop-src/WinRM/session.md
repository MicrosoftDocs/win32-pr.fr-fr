---
title: Objet session (WSManDisp. h)
description: Définit des opérations et des paramètres de session.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Windows Remote Management d’objet de Session
- Windows Remote Management d’objet de Session, description
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b63ce9aa5898f3b6dad716f7af19688059ccf7a3f48901fa73ed3250cd2660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121559"
---
# <a name="session-object-wsmandisph"></a>Objet session (WSManDisp. h)

Définit des opérations et des paramètres de session. toute opération de Windows Remote Management nécessite la création d’une **Session** qui se connecte à un ordinateur distant, à un [*contrôleur de gestion de base*](windows-remote-management-glossary.md) (BMC) ou à l’ordinateur local. Les opérations de réseau WinRM incluent l’obtention, l’écriture ou l’énumération de données, ou l’appel de méthodes. Les méthodes de l’objet de **session** reflètent les opérations de base définies dans le protocole WS-Management.

## <a name="members"></a>Membres

L’objet **session** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **session** possède ces méthodes.



| Méthode                                 | Description                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Créer**](session-create.md)       | Crée une nouvelle instance d’une ressource et retourne l’URI du nouvel objet.<br/>                                      |
| [**Supprimer**](session-delete.md)       | Supprime la ressource spécifiée dans l’URI de ressource.<br/>                                                              |
| [**Énumérer**](session-enumerate.md) | Énumère les ressources d’une collection, d’une table ou d’un journal des messages.<br/>                                                         |
| [**Télécharger**](session-get.md)             | Récupère une ressource du service et retourne une représentation XML de l’instance actuelle de la ressource.<br/> |
| [**Repérer**](session-identify.md)   | Interroge un ordinateur distant pour déterminer s’il prend en charge le protocole WS-Management<br/>                                 |
| [**Appeler**](session-invoke.md)       | Appelle une méthode qui retourne les résultats de l’appel de méthode.<br/>                                                    |
| [**Posé**](session-put.md)             | Met à jour une ressource.<br/>                                                                                              |



 

### <a name="properties"></a>Propriétés

L’objet **session** possède ces propriétés.



| Propriété                                            | Type d’accès           | Description                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchItems**](session-batchitems.md)<br/> | Lecture/écriture<br/> | Définit et obtient le nombre d’éléments dans chaque lot d’énumération. Cette valeur ne peut pas être modifiée pendant une énumération. Par défaut, la valeur par défaut est un nombre illimité d’éléments. Le fournisseur de ressources peut définir une limite.<br/> |
| [**Erreur**](session-error.md)<br/>           | Lecture seule<br/>  | Obtient des informations supplémentaires sur l’erreur dans un flux XML.<br/>                                                                                                                                                              |
| [**Expiré**](session-timeout.md)<br/>       | Lecture/écriture<br/> | Définit et obtient la durée maximale (en millisecondes) d’attente de l’application cliente.<br/>                                                                                                                   |



 

## <a name="remarks"></a>Remarques

L’objet **session** correspond à l’interface [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant montre comment créer un objet de **session** .


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API de script WinRM](winrm-scripting-api.md)
</dt> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





