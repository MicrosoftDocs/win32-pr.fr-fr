---
description: Les constantes suivantes sont utilisées par l’API de protection des données CNG.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Constantes CNG CNG (NCryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afc589afa113250728b46639b7cd47442034f7b3bc82264099f334919a94c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908797"
---
# <a name="cng-dpapi-constants"></a>Constantes CNG CNG

Les constantes suivantes sont utilisées par l’API de protection des données CNG.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**\_délimiteur de la description NCRYPT \_ \_ et**
</dt> <dd> <dl> <dt>

L "ET"
</dt> <dt>



Peut être utilisé pour tester une chaîne de descripteur de protection pour un et un délimiteur.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**le \_ descr \_ est égal à**
</dt> <dd> <dl> <dt>

L "="
</dt> <dt>



Peut être utilisé pour tester une chaîne de descripteur de protection pour un signe égal.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**\_délimiteur de la description NCRYPT \_ \_ ou**
</dt> <dd> <dl> <dt>

L "OU"
</dt> <dt>



Peut être utilisé pour tester une chaîne de descripteur de protection pour un délimiteur ou.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_algorithme de protection de clé NCRYPT \_ \_ \_ local**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



Le descripteur de protection LOCAL protège le contenu de l’ouverture de session, de l’utilisateur actuel ou de l’ordinateur local, tel qu’il est identifié par les constantes suivantes :

-   **\_protection de clé NCRYPT \_ \_ \_ connexion locale**
-   **\_protection de clé NCRYPT \_ \_ \_ utilisateur local**
-   **\_ \_ ordinateur local de protection de clé NCRYPT \_ \_**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**\_ \_ \_ SDDL algorithme de protection de clé NCRYPT \_**
</dt> <dd> <dl> <dt>

SDDL
</dt> <dt>



Protège le contenu d’une chaîne SDDL (Security Descriptor Definition Language) qui contient des informations de descripteur de sécurité.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_SID de \_ l' \_ algorithme de protection de clé NCRYPT \_**
</dt> <dd> <dl> <dt>

SID
</dt> <dt>



Le descripteur de protection SID contient un groupe ou une identité de principal.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_ \_ \_ informations d’identification de l’algorithme de protection de clé NCRYPT \_**
</dt> <dd> <dl> <dt>

« Informations d’identification webconnexion »
</dt> <dt>



Protège les informations d’identification du compte Web d’un utilisateur.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_protection de clé NCRYPT \_ \_ \_ connexion locale**
</dt> <dd> <dl> <dt>

horaire
</dt> <dt>



Protège le contenu de l’ouverture de session actuelle. Les utilisateurs ne seront pas en mesure de déchiffrer le contenu protégé après la déconnexion ou le redémarrage.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ ordinateur local de protection de clé NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

usinage
</dt> <dt>



Protège le contenu de l’ordinateur local. Tous les utilisateurs de l’ordinateur local peuvent déchiffrer le contenu protégé.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_protection de clé NCRYPT \_ \_ \_ utilisateur local**
</dt> <dd> <dl> <dt>

"user" (utilisateur)
</dt> <dt>



Protège le contenu de la session utilisateur en cours. Seul cet utilisateur sur l’ordinateur local sera en mesure de déchiffrer le contenu protégé.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_fournisseur de \_ protection de clés MS \_**
</dt> <dd> <dl> <dt>

« Fournisseur de protection de clé Microsoft »
</dt> <dt>



Représente le fournisseur de protection de clés Microsoft qui prend en charge les formats représentés par les constantes suivantes :

-   **\_SID de \_ l' \_ algorithme de protection de clé NCRYPT \_**
-   **\_algorithme de protection de clé NCRYPT \_ \_ \_ local**
-   **\_ \_ \_ SDDL algorithme de protection de clé NCRYPT \_**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_fournisseur de \_ protection de clé client \_ Windows \_**
</dt> <dd> <dl> <dt>

« fournisseur de Protection de clé de Client Windows »
</dt> <dt>



Représente le fournisseur de protection de clé Microsoft qui est disponible uniquement sur le client et qui prend en charge les formats représentés par les constantes suivantes :

-   **\_ \_ \_ informations d’identification de l’algorithme de protection de clé NCRYPT \_**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NCryptprotect. h</dt> </dl> |



 

 




