---
title: Noms principaux
description: Pour qu’un client crée une session mutuellement authentifiée avec un programme serveur, il doit fournir le nom principal attendu du serveur.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554ffecff6eb019b4712e6b2d9f5c6319db492e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462411"
---
# <a name="principal-names"></a>Noms principaux

Pour qu’un client crée une session mutuellement authentifiée avec un programme serveur, il doit fournir le nom principal attendu du serveur. Certains protocoles, tels que Kerberos, requièrent un nom principal de serveur correct pour toute session authentifiée. Un principal est une entité que le système de sécurité reconnaît. Cela comprend les utilisateurs humains et les services système. Tous les noms principaux prennent le même format pour un fournisseur SSP (Security Support Provider) donné. Un SSP est un module logiciel qui effectue la validation de la sécurité. Pour plus d’informations, consultez [vue d’ensemble de l’architecture SSPI](sspi-architectural-overview.md). Pour assurer l’uniformité, un fournisseur de sécurité fournit généralement des noms de services système similaires à ceux des utilisateurs. Sous certains fournisseurs de sécurité, les services système peuvent ne pas avoir de nom principal.

Le serveur inscrit son nom principal pour le fournisseur de sécurité à l’aide de la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) . Un seul nom de principal du serveur peut être utilisé pour chaque fournisseur de sécurité. Si plusieurs noms sont inscrits, un nom est choisi et utilisé de manière aléatoire. Le fournisseur de services partagés détermine le format du nom du principal. Par exemple, les SSP Kerberos/Negotiate pour un service système se présentent approximativement comme suit : nom de l’ordinateur \_ $ @childdomain.parentdomain1.parentdomain2.COM .

La procédure recommandée pour générer des noms principaux consiste à utiliser des API documentées (telles que la fonction **DsMakeSpn** ), au lieu de accolant ensemble le nom principal des chaînes. L’utilisation d’API documentées augmente la portabilité entre les différents environnements de déploiement et élimine les risques d’erreurs.

La spécification d’un nom de principal incorrect peut empêcher le client et le serveur d’établir une session authentifiée. Le SSP SCHANNEL prend les noms principaux sous l’une des deux formes suivantes :

-   Le premier formulaire de nom de principal SCHANNEL est le formulaire [*msstd*](m-glos.md) . Les noms sous la forme msstd suivent généralement le modèle msstd:servername@serverdomain.com . C’est ce qu’on appelle une propriété de nom d’adresse de messagerie. Si le certificat contient une propriété de nom de messagerie et qu’il contient le signe arobase (@), le nom du principal est msstd : email Name. Dans le cas contraire, elle doit contenir la propriété nom commun. Les barres obliques inverses internes sont doublées, tout comme dans les liaisons de chaîne.
-   Le deuxième formulaire de nom de principal SCHANNEL est le formulaire [*fullsic*](f-glos.md) . Il s’agit d’une série de noms conformes RFC1779 délimités par des crochets pointus et séparés par des barres obliques inverses. En règle générale, elle suit le modèle fullsic : \\ < \\ Authority \\ \\ . \\ ... Person> ou fullsic : \\ < \\ autorité de certification \\ \\ ... \\ . ServerProgram>.

Si le nom ne correspond pas au certificat, l’erreur \_ accès \_ refusé est retournée. Si le format du nom n’est pas valide, SCHANNEL SSP retourne le \_ paramètre non valide de l’erreur de code \_ .

Pour rechercher le nom principal du serveur, les applications peuvent appeler [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname). Cela alloue une chaîne terminée par le caractère null pour contenir le nom du principal. Avant qu’elle ne se termine, votre application doit appeler [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) pour libérer la mémoire occupée par cette chaîne.

L’interrogation du nom du serveur de cette manière n’est pas sécurisée et doit être évitée. Pour l’authentification du serveur, le programme client doit connaître le serveur auquel il se connecte et créer le nom principal du serveur à partir de zéro.

 

 




