---
description: Vous pouvez spécifier un descripteur de sécurité pour un canal nommé quand vous appelez la fonction CreateNamedPipe. Le descripteur de sécurité contrôle l’accès aux terminaisons client et serveur du canal nommé.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Sécurité des canaux nommés et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556987cf35845de249bf0e19f3a0b481aab18e891c3b6211f26eb51571704d7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451209"
---
# <a name="named-pipe-security-and-access-rights"></a>Sécurité des canaux nommés et droits d’accès

Windows security vous permet de contrôler l’accès aux canaux nommés. Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model).

Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptors) pour un canal nommé quand vous appelez la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Le descripteur de sécurité contrôle l’accès aux terminaisons client et serveur du canal nommé. Si vous spécifiez **null**, le canal nommé obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès dans le descripteur de sécurité par défaut pour un canal nommé accordent un contrôle total au compte LocalSystem, aux administrateurs et au propriétaire créateur. Ils accordent également un accès en lecture aux membres du groupe tout le monde et du compte anonyme.

Pour récupérer le descripteur de sécurité d’un canal nommé, appelez la fonction [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Pour modifier le descripteur de sécurité d’un canal nommé, appelez la fonction [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Lorsqu’un thread appelle [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) pour ouvrir un handle à l’extrémité serveur d’un canal nommé existant, le système effectue une vérification d’accès avant de retourner le handle. La vérification d’accès compare le jeton d’accès du thread et les [droits d’accès](/windows/desktop/SecAuthZ/access-rights-and-access-masks) demandés à la liste DACL dans le descripteur de sécurité du canal nommé. En plus des droits d’accès demandés, la DACL doit autoriser l' \_ \_ accès de l’instance de création de canal du fichier de thread appelant \_ au canal nommé.

De même, lorsqu’un client appelle la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) pour se connecter à l’extrémité cliente d’un canal nommé, le système effectue une vérification d’accès avant d’accorder l’accès au client.

Le handle retourné par la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) a toujours un accès Synchronize. Il possède également une \_ lecture générique, une \_ écriture générique, ou les deux, selon le mode d’ouverture du canal. Voici les droits d’accès pour chaque mode ouvert.



| Mode d’ouverture                           | Droits d’accès                                              |
|-------------------------------------|------------------------------------------------------------|
| DUPLEX d’accès du canal \_ \_ (0x00000003)   | FICHIER \_ de \_ lecture générique, \_ écriture générique de fichier \_ et synchroniser |
| \_Accès au canal \_ entrant (0x00000001)  | \_ \_ Lecture et synchronisation génériques de fichier                        |
| \_Accès au canal \_ sortant (0x00000002) | \_ \_ Écriture et synchronisation génériques des fichiers                       |



 

FICHIER \_ générique \_ accès en lecture pour un canal nommé combine les droits de lecture des données du canal, de lecture des attributs de canal, de lecture des attributs étendus et de lecture de la liste DACL du canal.

FICHIER \_ générique \_ accès en écriture pour un canal nommé combine les droits d’écriture de données dans le canal, y ajoute des données, écrit des attributs de canal, écrit des attributs étendus et lit la liste DACL du canal. Étant donné \_ que \_ les données d’ajout de fichier et \_ l’instance de création de canal de fichier \_ \_ ont la même définition, le fichier \_ \_ écriture générique active l’autorisation de créer le canal. Pour éviter ce problème, utilisez les droits individuels au lieu d’utiliser l' \_ écriture générique de fichier \_ .

Vous pouvez demander le \_ \_ droit d’accès à la sécurité du système d’accès à un objet de canal nommé si vous souhaitez lire ou écrire la liste SACL de l’objet. Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Pour empêcher les utilisateurs distants ou les utilisateurs d’une autre session des services Terminal Server d’accéder à un canal nommé, utilisez le SID d’ouverture de session sur la liste DACL pour le canal. Le SID d’ouverture de session est également utilisé dans les ouvertures de session d’exécution. Il s’agit du SID utilisé pour protéger l’espace de noms d’objet par session. Pour plus d’informations, consultez [obtention du SID d’ouverture de session en C++](/previous-versions//aa446670(v=vs.85)).

 

 
