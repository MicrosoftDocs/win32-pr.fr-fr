---
description: Un privilège est le droit d’un compte, tel qu’un compte d’utilisateur ou de groupe, d’effectuer diverses opérations liées au système sur l’ordinateur local, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système.
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: Privilèges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0289ea66f4c1d2f94cb74112a1160dd93cc873125ae5183bd6a6fab5834b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912135"
---
# <a name="privileges"></a>Privilèges

Un [*privilège*](/windows/desktop/SecGloss/p-gly) est le droit d’un compte, tel qu’un compte d’utilisateur ou de groupe, d’effectuer diverses opérations liées au système sur l’ordinateur local, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système. Les privilèges diffèrent des droits d’accès de deux manières :

-   Les privilèges contrôlent l’accès aux ressources système et aux tâches système, tandis que les droits d’accès contrôlent l’accès aux [objets sécurisables](securable-objects.md).
-   Un administrateur système affecte des privilèges aux comptes d’utilisateurs et de groupes, tandis que le système autorise ou refuse l’accès à un objet sécurisable en fonction des droits d’accès accordés dans les ACE dans la liste DACL de l’objet.

Chaque système possède une base de données de comptes qui stocke les privilèges détenus par les comptes d’utilisateurs et de groupes. Lorsqu’un utilisateur ouvre une session, le système génère un [jeton d’accès](access-tokens.md) qui contient une liste des privilèges de l’utilisateur, y compris ceux accordés à l’utilisateur ou aux groupes auxquels l’utilisateur appartient. Notez que les privilèges s’appliquent uniquement à l’ordinateur local ; un compte de domaine peut avoir des privilèges différents sur des ordinateurs différents.

Lorsque l’utilisateur tente d’effectuer une opération privilégiée, le système vérifie le jeton d’accès de l’utilisateur pour déterminer si l’utilisateur détient les privilèges nécessaires. dans ce cas, il vérifie si les privilèges sont activés. Si les tests de l’utilisateur échouent, le système n’effectue pas l’opération.

Pour déterminer les privilèges détenus dans un jeton d’accès, appelez la fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) , qui indique également quels privilèges sont activés. La plupart des privilèges sont désactivés par défaut.

l’API Windows définit un ensemble de constantes de chaîne, telles que \_ SE \_ nom ASSIGNPRIMARYTOKEN, pour identifier les différents privilèges. Ces constantes sont les mêmes sur tous les systèmes et sont définies dans Winnt. h. pour obtenir un tableau des privilèges définis par Windows, consultez [constantes de privilège](authorization-constants.md). Toutefois, les fonctions qui obtiennent et ajustent les privilèges dans un jeton d’accès utilisent le type [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) pour identifier les privilèges. Les valeurs **LUID** d’un privilège peuvent différer d’un ordinateur à un autre, et d’un démarrage à un autre sur le même ordinateur. Pour récupérer le **LUID** actuel qui correspond à l’une des constantes de chaîne, utilisez la fonction [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) . Utilisez la fonction [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) pour convertir un **LUID** en sa constante de chaîne correspondante.

Le système fournit un ensemble de noms d’affichage qui décrivent chacun des privilèges. Elles sont utiles lorsque vous devez afficher une description d’un privilège pour l’utilisateur. Utilisez la fonction [**LookupPrivilegeDisplayName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) pour récupérer une chaîne de description qui correspond à la constante de chaîne pour un privilège. par exemple, sur les systèmes qui utilisent l’anglais (états-unis), le nom d’affichage du \_ \_ privilège SE nom SYSTEMTIME est « modifier l’heure système ».

Vous pouvez utiliser la fonction [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) pour déterminer si un jeton d’accès contient un jeu de privilèges spécifié. Cela s’avère particulièrement utile pour les applications serveur qui empruntent l’identité d’un client.

Un administrateur système peut utiliser des outils d’administration, tels que le gestionnaire des utilisateurs, pour ajouter ou supprimer des privilèges pour les comptes d’utilisateurs et de groupes. Les administrateurs peuvent utiliser les fonctions de l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) par programmation pour travailler avec des privilèges. Les fonctions [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) et [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) ajoutent ou suppriment des privilèges d’un compte. La fonction [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) énumère les privilèges détenus par un compte spécifié. La fonction [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) énumère les comptes qui contiennent un privilège spécifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes d’autorisation](authorization-constants.md)
</dt> <dt>

[Activation et désactivation des privilèges en C++](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 
