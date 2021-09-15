---
description: Permet à un client de gérer les paramètres de quota de disque global d’un volume NTFS. cet objet rend les fonctionnalités essentielles de l’interface DIDiskQuotaUser disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.
title: Objet DIDiskQuotaUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412552"
---
# <a name="didiskquotauser-object"></a>Objet DIDiskQuotaUser

Permet à un client de gérer les paramètres de quota de disque global d’un volume NTFS. cet objet rend les fonctionnalités essentielles de l’interface **DIDiskQuotaUser** disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.

## <a name="members"></a>Membres

L’objet **DIDiskQuotaUser** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **DIDiskQuotaUser** a ces méthodes.



| Méthode                                           | Description                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**Invalidate**](didiskquotauser-invalidate.md) | Efface les informations utilisateur mises en cache de l’objet.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **DIDiskQuotaUser** a ces propriétés.



| Propriété                                                                        | Type d’accès           | Description                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**AccountContainerName**](didiskquotauser-accountcontainername.md)<br/> | Lecture seule<br/>  | Obtient le nom du conteneur de compte de l’utilisateur.<br/>                                            |
| [**AccountStatus**](didiskquotauser-accountstatus.md)<br/>               | Lecture seule<br/>  | Obtient l’état du compte de l’utilisateur.<br/>                                                    |
| [**NomComplet**](didiskquotauser-displayname.md)<br/>                   | Lecture seule<br/>  | Obtient le nom complet de l’utilisateur.<br/>                                                             |
| [**id**](didiskquotauser-id.md)<br/>                                     | Lecture seule<br/>  | Obtient un ID qui identifie de façon unique l’utilisateur.<br/>                                             |
| [**LogonName**](didiskquotauser-logonname.md)<br/>                       | Lecture seule<br/>  | Obtient le nom du compte d’ouverture de session de l’utilisateur.<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | Lecture/écriture<br/> | Définit ou obtient la [**limite de quota**](diskquotacontrol-object.md)actuelle de l’utilisateur.<br/>           |
| [**QuotaLimitText**](didiskquotauser-quotalimittext.md)<br/>             | Lecture seule<br/>  | Obtient la [**limite de quota**](diskquotacontrol-object.md) actuelle de l’utilisateur sous la forme d’une chaîne de texte. <br/> |
| [**QuotaThreshold**](didiskquotauser-quotathreshold.md)<br/>             | Lecture/écriture<br/> | Définit ou obtient le seuil d’avertissement de l’utilisateur, en octets.<br/>                                      |
| [**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)<br/>     | Lecture seule<br/>  | Obtient le seuil d’avertissement de l’utilisateur sous la forme d’une chaîne de texte.<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | Lecture seule<br/>  | Obtient l’utilisation actuelle du disque de l’utilisateur, en octets.<br/>                                             |
| [**QuotaUsedText**](didiskquotauser-quotausedtext.md)<br/>               | Lecture seule<br/>  | Obtient l’utilisation du disque actuel de l’utilisateur sous la forme d’une chaîne de texte.<br/>                                      |



 

## <a name="remarks"></a>Notes

Chaque utilisateur sur le volume qui est géré par l’objet [**DiskQuotaControl**](diskquotacontrol-object.md) est associé à un objet **DIDiskQuotaUser** . Cet objet permet à un client de gérer les paramètres d’un utilisateur individuel. Il existe plusieurs façons d’obtenir l’objet **DIDiskQuotaUser** d’un utilisateur :

-   Les objets **DIDiskQuotaUser** pour tous les utilisateurs avec quotas sur le volume sont exposés en tant que collection et peuvent être énumérés. Vous trouverez ci-dessous une discussion sur l’énumération des objets **DIDiskQuotaUser** .
-   Lorsque vous ajoutez un nouvel utilisateur, la méthode [**adduser**](diskquotacontrol-adduser.md) retourne l’objet **DIDiskQuotaUser** de l’utilisateur.
-   Si vous avez le nom de l’utilisateur, la méthode [**FindUser**](diskquotacontrol-finduser.md) retourne l’objet **DIDiskQuotaUser** de l’utilisateur.

### <a name="enumerating-disk-quota-users"></a>Énumération des utilisateurs du quota de disque

Les objets **DIDiskQuotaUser** pour tous les utilisateurs avec un quota sur le volume sont exposés en tant que collection. L’objet [**DiskQuotaControl**](diskquotacontrol-object.md) exporte une méthode d’énumérateur standard qui vous permet d’énumérer la collection d’objets **DIDiskQuotaUser** . la procédure suivante montre comment effectuer l’énumération avec Microsoft JScript (compatible avec la spécification du langage ECMA 262). vous pouvez utiliser une procédure similaire avec Visual Basic ou Microsoft Visual Basic scripting Edition (VBScript).

1.  Créez un nouvel objet [**DiskQuotaControl**](diskquotacontrol-object.md) .
2.  Initialisez-le avec [**Initialize**](diskquotacontrol-initialize.md).
3.  créez un nouvel objet **énumérateur** JScript.
4.  Utilisez une boucle **for** pour énumérer les objets **DIDiskQuotaUser** . Il n’est pas nécessaire de définir une valeur de départ. La méthode **MoveNext** de l’objet Enumerator indique à la méthode **Item** de retourner l’objet **DIDiskQuotaUser** suivant. La méthode **atEnd** retourne la **valeur false** lorsque vous atteignez la fin de la liste.
5.  Si nécessaire, utilisez l’objet **DIDiskQuotaUser** retourné par la méthode **Item** de l’énumérateur pour récupérer ou définir une ou plusieurs des propriétés de quota de disque de l’utilisateur associé.

Le fragment de code suivant montre comment énumérer les objets **DIDiskQuotaUser** avec JScript. L’argument de **\_ nom de volume** qui est passé à la fonction **EnumUsers** est une valeur de chaîne contenant un nom de volume tel que « C : \\ \\ ».


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



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

 

 




