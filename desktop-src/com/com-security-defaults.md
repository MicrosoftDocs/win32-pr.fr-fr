---
title: Valeurs par défaut de sécurité COM
description: Vous pouvez utiliser les valeurs par défaut de sécurité COM pour votre application au lieu de spécifier vos propres paramètres de sécurité.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309293"
---
# <a name="com-security-defaults"></a>Valeurs par défaut de sécurité COM

Vous pouvez utiliser les valeurs par défaut de sécurité COM pour votre application au lieu de spécifier vos propres paramètres de sécurité. Dans ce cas, COM initialise et gère la sécurité pour vous. Vous n’avez pas besoin de configurer le registre ou d’appeler des fonctions de sécurité dans votre programme.

Toutefois, si certaines valeurs nommées du Registre ont été définies ou modifiées, les valeurs par défaut de sécurité utilisées par COM seront affectées. La liste ci-dessous décrit les valeurs par défaut de la sécurité COM et explique comment certaines valeurs sont influencées par les paramètres du Registre.

Voici les valeurs de sécurité par défaut utilisées par COM :

-   Le fournisseur de services de sécurité par défaut est celui qui est déterminé par COM comme étant le plus compatible avec l’environnement. COM choisit le protocole Kerberos V5 ou NTLMSSP, le protocole Kerberos étant le choix par défaut. Aucun des protocoles fournis par Schannel n’est jamais choisi par défaut.
-   Le système identifie un appelant par le biais du nom d’utilisateur et du mot de passe et crée automatiquement un jeton d’identification utilisé par le système de sécurité.
-   Si la valeur nommée [LegacyAuthenticationLevel](legacyauthenticationlevel.md) existe et si sa valeur a été définie, cette valeur est utilisée. Dans le cas contraire, le niveau d’authentification est défini sur Connect ( \_ \_ connexion au niveau Authn C RPC \_ \_ ). Ce niveau signifie que lors du premier appel d’un client vers le serveur, COM effectue un contrôle d’authentification. Si le client réussit la vérification, aucune autre authentification n’est effectuée. La valeur AuthenticationLevel peut également être définie sous la clé [AppID](appid-key.md) .
-   Si la valeur nommée [LegacyImpersonationLevel](legacyimpersonationlevel.md) existe et si sa valeur a été définie, cette valeur est utilisée. Dans le cas contraire, le niveau d’emprunt d’identité est défini pour identifier (RPC \_ C \_ IMP \_ Level \_ identifier). Les droits d’emprunt d’identité sont accordés par le client au serveur. L’identification du niveau signifie que le serveur peut obtenir l’identité du client. Le serveur peut emprunter l’identité du client pour la vérification de la liste de contrôle d’accès (ACL), mais ne peut pas accéder aux objets système en tant que client. Pour plus d’informations, consultez [niveaux d’emprunt d’identité](impersonation-levels.md) et [masquage](cloaking.md).
-   Si la valeur nommée [AccessPermission](accesspermission.md) sous **AppID** existe et qu’elle a été définie, cette valeur est utilisée. Dans le cas contraire, COM recherche une entrée [DefaultAccessPermission](defaultaccesspermission.md) . S’il est présent, cette valeur est utilisée. Si cette valeur n’est pas présente, COM construit une liste de contrôle d’accès qui accorde des autorisations à l’identité du serveur et au système local.
-   Si la valeur nommée [SRPTrustLevel](srptrustlevel.md) sous **AppID** existe et qu’elle a été définie, cette valeur est utilisée. Dans le cas contraire, le niveau de confiance de la stratégie de restriction logicielle (SRP) est défini sur non autorisé (sécurité \_ LEVELID non \_ autorisée), ce qui indique que l’application est exécutée dans un environnement limité et n’est pas autorisée à accéder à des privilèges d’utilisateur sensibles à la sécurité de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




