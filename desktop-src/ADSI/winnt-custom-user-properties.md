---
title: Propriétés de l’utilisateur personnalisé Winnt
description: Le fournisseur Winnt met à disposition les propriétés personnalisées suivantes pour la classe utilisateur. Elles sont accessibles par le biais des méthodes IADs. obten et IADs. put. Pour plus d’informations, consultez la \_ structure User info \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Propriétés de l’utilisateur personnalisé Winnt ADSI
- Fournisseur WinNT ADSI, objet utilisateur, propriétés personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941367"
---
# <a name="winnt-custom-user-properties"></a>Propriétés de l’utilisateur personnalisé Winnt

Le fournisseur Winnt met à disposition les propriétés personnalisées suivantes pour la classe utilisateur. Elles sont accessibles par le biais des méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) . Pour plus d’informations, consultez la structure [**User \_ info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .



| Propriété            | Type         | Description                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | String       | Lecteur du répertoire de démarrage de l’utilisateur. Pointeur vers une chaîne Unicode qui spécifie le chemin d’accès du répertoire de départ. La chaîne peut être **null**. Consultez l’exemple de cette rubrique.                                                                                                                                                                                 |
| **ObjectSID**       | Chaîne d’octets | SID de l’objet de l’utilisateur. Pour obtenir un exemple de récupération du SID de l’objet à l’aide du fournisseur WinNT, consultez [SID d’objet (fournisseur WinNT)](object-sid.md) .                                                                                                                                                                                                          |
| **Paramètres**      | String       | Paramètres de l’utilisateur. Pointe vers une chaîne Unicode qui est réservée à une utilisation par des applications. Cette chaîne peut être une chaîne NULL, ou elle peut contenir un nombre quelconque de caractères avant le caractère null de fin. Les produits Microsoft utilisent ce membre pour stocker les données de configuration de l’utilisateur. Cette propriété ne peut être modifiée que par une application au cours de l’installation. |
| **Mot de passe**     | Temps         | Durée d’utilisation du mot de passe. Cette propriété indique le nombre de secondes qui se sont écoulées depuis la dernière modification du mot de passe.                                                                                                                                                                                                                    |
| **PasswordExpired** | Integer      | Indique quand le mot de passe a expiré. Quand vous utilisez l’opération obtenir, la valeur zéro est retournée si le mot de passe n’a pas expiré, ou une valeur différente de zéro si elle a expiré. Consultez l’exemple de cette rubrique.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Integer      | ID de groupe principal de l’utilisateur, par exemple, l’ID de groupe d’utilisateurs de domaine. Consultez l’exemple de cette rubrique.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Integer      | Indicateur utilisateur défini dans [**l' \_ \_ \_ énumération de l’indicateur utilisateur ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum). Pour obtenir un exemple d’utilisation de UserFlags, consultez [mot de passe n’expire jamais (fournisseur WinNT)](winnt-password-never-expires.md) .                                                                                                                                                             |



 

Cet exemple montre comment définir le répertoire du lecteur de démarrage d’un utilisateur.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



Cet exemple montre comment utiliser PasswordExpired pour forcer un utilisateur à modifier le mot de passe à la prochaine ouverture de session.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



Cet exemple montre comment récupérer le groupe principal de l’utilisateur.


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 