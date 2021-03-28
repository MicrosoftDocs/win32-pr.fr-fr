---
description: Permet à un administrateur de gérer les propriétés de quota de disque d’un volume.
title: Objet DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 843f33ee79e70309a47f170bb1935f94f45c8f2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991673"
---
# <a name="diskquotacontrol-object"></a>Objet DiskQuotaControl

Permet à un administrateur de gérer les propriétés de quota de disque d’un volume. Le système de fichiers NTFS permet à un administrateur de gérer l’utilisation du disque sur un volume partagé en allouant une quantité d’espace disque spécifiée ou une *limite de quota* à chaque utilisateur. Vous pouvez utiliser cet objet pour définir la limite de quota par défaut qui sera automatiquement affectée à tous les nouveaux utilisateurs.

## <a name="members"></a>Membres

L’objet **DiskQuotaControl** possède les types de membres suivants :

-   [Événements](#events)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

L’objet **DiskQuotaControl** contient ces événements.



| Événement                                                           | Description                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | Se produit lorsque les informations de nom d’un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) ont été résolues.<br/> |



 

### <a name="methods"></a>Méthodes

L’objet **DiskQuotaControl** a ces méthodes.



| Méthode                                                                                    | Description                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Affecte un quota de disque autre que celui par défaut à un nouvel utilisateur.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Supprime un utilisateur du volume.<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | Recherche l’entrée d’un utilisateur, par son nom, dans le fichier de quota du volume.<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Place l’objet utilisateur spécifié en regard de la résolution de nom.<br/>              |
| [**Initialiser**](diskquotacontrol-initialize.md)                                         | Ouvre un volume spécifié et initialise son objet de contrôle de quota.<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | Invalide le cache du nom d’utilisateur de l’ID de sécurité.<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | Arrête le thread de résolution de nom d’utilisateur.<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | Convertit un nom d’ouverture de session en ID de sécurité de l’utilisateur correspondant au format de chaîne.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **DiskQuotaControl** a ces propriétés.



| Propriété                                                                                   | Type d’accès           | Description                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Lecture/écriture<br/> | Définit ou obtient la limite de quota par défaut.<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Lecture seule<br/>  | Obtient la limite de quota par défaut sous la forme d’une chaîne de texte.<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Lecture/écriture<br/> | Définit ou obtient le seuil de quota par défaut.<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Lecture seule<br/>  | Obtient le seuil de quota par défaut sous la forme d’une chaîne de texte.<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Lecture/écriture<br/> | Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse sa limite de quota affectée.<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Lecture/écriture<br/> | Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse son seuil de quota attribué.<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Lecture seule<br/>  | Obtient une valeur booléenne qui indique si le fichier de quota du volume est terminé.<br/>                                                             |
| [**QuotaFileRebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Lecture seule<br/>  | Obtient une valeur booléenne qui indique si le fichier de quota du volume est en cours de reconstruction.<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | Lecture/écriture<br/> | Définit ou obtient l’état des quotas de disque du volume.<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | Lecture/écriture<br/> | Définit ou obtient une valeur qui contrôle la façon dont le SID de l’utilisateur est résolu en noms d’utilisateurs.<br/>                                                                        |



 

## <a name="remarks"></a>Notes

Un administrateur peut utiliser l’objet **DiskQuotaControl** pour effectuer un certain nombre de tâches, y compris les éléments suivants :

-   Activation et désactivation du système de quota de disque du volume.
-   Obtention de l’état du système de quota sur le volume.
-   Refus de l’espace disque aux utilisateurs dépassant leur limite de quota.
-   Spécification du seuil d’avertissement et des valeurs de limite de quota par défaut qui seront affectés aux nouveaux utilisateurs.
-   Ajout et suppression d’utilisateurs.

L’objet **DiskQuotaControl** vous permet de définir des valeurs globales par défaut pour le volume pour les propriétés telles que les limites de quota. Toutefois, chaque utilisateur est représenté par un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) qui peut être utilisé pour spécifier des paramètres de quota individuels.

Il existe plusieurs façons d’obtenir l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) d’un utilisateur :

-   Les objets [**DIDiskQuotaUser**](didiskquotauser-object.md) pour tous les utilisateurs avec quotas sur le volume sont exposés en tant que collection et peuvent être énumérés. Pour plus d’informations sur l’énumération des objets **DIDiskQuotaUser** , consultez la section **énumération des quotas de disque** pour les utilisateurs dans la section Notes de **DIDiskQuotaUser**.
-   Lorsque vous ajoutez un nouvel utilisateur, la méthode [**adduser**](diskquotacontrol-adduser.md) retourne l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.
-   Si vous avez le nom de l’utilisateur, la méthode [**FindUser**](diskquotacontrol-finduser.md) retourne l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.

Cet objet rend les fonctionnalités essentielles de l’interface IDiskQuotaControl disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Shell**](shell.md)
</dt> </dl>

 

 




