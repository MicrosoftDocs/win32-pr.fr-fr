---
title: mise à jour corrective des logiciels de jeu dans Windows XP, Windows Vista et Windows 7
description: cet article examine certaines méthodes de mise à jour corrective qui fonctionnent correctement dans Windows Vista et Windows 7, ainsi que Windows XP.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dae9b3bc91c96006f3b2117093962ee485db948fd983191f2db3c7f88fb33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042499"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>mise à jour corrective des logiciels de jeu dans Windows XP, Windows Vista et Windows 7

Windows Vista et Windows 7 ont un certain nombre de fonctionnalités pour renforcer la sécurité du système d’exploitation. La sécurité ajoutée signifie que l’application de correctifs logiciels n’est pas aussi simple que dans le passé. cet article examine certaines méthodes de mise à jour corrective qui fonctionnent correctement dans Windows Vista et Windows 7, ainsi que Windows XP.

Il existe deux catégories principales de jeux nécessitant des correctifs :

-   Jeux nécessitant uniquement des correctifs occasionnels, tels que la plupart des jeux hors connexion.
-   Jeux nécessitant des correctifs fréquents, tels que la plupart des jeux en ligne.

cet article offre également une brève introduction au contrôle de compte d’utilisateur (UAC, User Account Control) pour servir d’arrière-plan sur les droits que les développeurs peuvent espérer avoir dans Windows Vista et Windows 7.

-   [Contrôle de compte d'utilisateur](#user-account-control)
-   [Jeux nécessitant uniquement des correctifs occasionnels](#games-that-require-only-occasional-patches)
    -   [méthode 1 : utiliser Windows Installer pour les correctifs occasionnels](#method-1-use-windows-installer-for-occasional-patches)
    -   [Méthode 2 : exiger des droits d’administrateur pour appliquer des correctifs](#method-2-require-administrator-rights-to-apply-patches)
-   [Jeux nécessitant des correctifs fréquents](#games-that-require-frequent-patches)
    -   [Méthode 3 : installation par utilisateur](#method-3-install-per-user)
    -   [Méthode 4 : installer dans un emplacement de Per-Computer commun](#method-4-install-to-a-common-per-computer-location)
    -   [Autres possibilités](#other-possibilities)
-   [Résumé](#summary)

## <a name="user-account-control"></a>Contrôle de compte d'utilisateur

Windows Vista et Windows 7 ont deux types principaux de comptes d’utilisateur : utilisateur Standard et administrateur. Un compte d’utilisateur standard a plusieurs restrictions d’accès ; par exemple, il ne peut pas écrire de données dans le système de fichiers dans% SystemDrive% \\ Program Files ou dans le registre de l' \_ ordinateur local HKEY \_ . Cela a des implications pour l’application des correctifs à un jeu s’il est installé dans un emplacement en lecture seule. contrairement à Windows XP, le compte d’utilisateur Standard est bien plus courant dans Windows Vista et Windows 7. Les comptes d’utilisateur standard sont également requis pour les fonctionnalités importantes du système d’exploitation, telles que les contrôles de contrôle parental. Les contrôles parentaux requièrent que le compte enfant soit un utilisateur standard et l’élévation d’un tel compte à l’administrateur pour un même jeu empêche le contrôle parental de fonctionner avec tous les autres jeux. C’est pourquoi il est important que les jeux soient conçus pour un utilisateur standard.

Windows Vista et Windows 7 ont un modèle plus récent pour les droits d’utilisateur, afin d’empêcher les utilisateurs d’exécuter des programmes qui tentent d’effectuer des opérations que l’utilisateur n’envisage pas ou n’autorisent pas. À cette fin, le contrôle de compte d’utilisateur (précédemment appelé compte d’utilisateur doté de privilèges minimum ou LUA) permet aux utilisateurs d’utiliser l’ordinateur avec des droits de bas niveau la plupart du temps, tout en étant en mesure d’exécuter facilement des applications qui nécessitent des droits de niveau supérieur, le cas échéant. Cela signifie que les comptes d’utilisateur standard et les comptes d’administrateur exécutent tous les deux des applications avec des droits d’utilisateur standard, mais seuls les comptes d’administrateur ont la possibilité d’accorder des droits élevés aux applications. Le système d’exploitation demande aux utilisateurs avec des comptes d’administrateur une autorisation explicite avant d’exécuter une application avec des droits élevés, et si un programme qui requiert des droits d’administrateur est exécuté sur un compte d’utilisateur standard, le système vous invite à confirmer l’approbation de l’administrateur.

## <a name="games-that-require-only-occasional-patches"></a>Jeux nécessitant uniquement des correctifs occasionnels

Certains jeux n’ont besoin que de quelques correctifs tout au long de leur cycle de vie. deux méthodes que vous pouvez utiliser pour cette fréquence de mise à jour corrective sont la distribution de correctifs en tant que packages de Windows Installer, ce qui ne nécessite généralement pas de droits d’administrateur ou d’utilisation d’un autre type de distribution qui modifie directement les fichiers de jeu.

> [!Note]  
> Indépendamment du fait qu’un jeu nécessite des mises à jour correctives fréquentes, les applications requièrent généralement l’installation ou la suppression des droits d’administrateur.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>méthode 1 : utiliser Windows Installer pour les correctifs occasionnels

dans cette méthode, un Windows Installer est utilisé pour installer un package (fichier .msi) et un correctif Windows Installer (fichier. msp) est distribué pour installer les correctifs. Le package doit avoir une table MsiPatchCertificate, et le correctif doit être signé numériquement par un certificat dans la table. Pour plus d’informations sur la signature numérique, consultez [signature Authenticode pour les développeurs de jeux](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

pour plus d’informations et pour connaître la configuration requise pour utiliser cette méthode de mise à jour, consultez la documentation Windows Installer :

-   [Correctifs et mises à niveau](/windows/desktop/Msi/patching-and-upgrades)
-   [Mise à jour corrective du contrôle de compte d’utilisateur (UAC)](/windows/desktop/Msi/user-account-control--uac--patching)

l’inconvénient de cette méthode est que si le jeu n’a pas été installé à partir d’un support amovible sur Windows XP, la mise à jour corrective nécessite des droits d’administrateur. toutefois, cela n’est probablement pas trop restrictif, car la plupart des administrateurs des utilisateurs sur Windows XP et la restriction aux logiciels installés à partir de supports amovibles n’est pas présente sur Windows Vista.

Le principal avantage de cette méthode est que les correctifs peuvent être appliqués par un compte d’utilisateur standard sans nécessiter d’invite ni d’authentification pour des droits élevés. Cela offre une meilleure expérience utilisateur, car pour jouer un jeu, un utilisateur disposant d’un compte d’utilisateur standard n’a pas besoin de demander à une personne disposant d’un compte d’administrateur pour installer le correctif ou de fournir au compte d’utilisateur standard des droits d’administrateur permanents.

il est possible que cette méthode fonctionne pour les jeux qui nécessitent des correctifs fréquents, mais la surcharge liée à l’utilisation d’Windows Installer packages, en termes d’intégration de build et de prise en charge d’un grand nombre de fichiers, peut rendre cette méthode moins souhaitable que d’autres.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Méthode 2 : exiger des droits d’administrateur pour appliquer des correctifs

Dans cette méthode, le fichier exécutable qui applique le correctif requiert des droits d’administrateur pour s’exécuter. Avec les droits d’administrateur, l’exécutable de mise à jour corrective peut modifier directement les fichiers de jeu situés dans% SystemDrive% \\ Program Files.

L’avantage de cette méthode est sa simplicité. Toutefois, cette méthode n’est pas appropriée si le jeu nécessite des correctifs fréquents, car si un utilisateur disposant d’un compte d’utilisateur standard souhaite jouer un jeu nécessitant des correctifs fréquents, comme un jeu en ligne massivement multi-joueurs, cet utilisateur a deux possibilités :

-   Demandez à un administrateur de se connecter et de corriger le jeu, ce qui peut être gênant pour les deux parties.
-   Faire en sorte que son compte soit définitivement élevé avec des droits d’administrateur.

> [!Note]  
> La dernière solution affaiblit non seulement la sécurité du système dans son ensemble, mais elle empêche les fonctionnalités importantes, telles que le contrôle parental, de fonctionner.

 

Lors de l’implémentation de cette méthode, le fichier exécutable qui applique le correctif doit être différent de l’exécutable du jeu. Le manifeste de l’exécutable de mise à jour corrective doit spécifier requireAdministrator pour requestedExecutionLevel pour le désigner comme une application qui requiert des droits d’administrateur. Pour plus d’informations sur la procédure à suivre, consultez [pratiques recommandées pour les développeurs et instructions pour les applications dans un environnement de moindre privilège](/previous-versions/dotnet/articles/aa480150(v=msdn.10)), dans « schéma de manifeste d’application ».

Lorsque cette méthode est utilisée, même avec les paramètres du manifeste, le fichier exécutable peut encore être lancé sans droits d’administrateur dans deux cas :

-   si le système d’exploitation est Windows XP et que le compte de l’utilisateur est un utilisateur restreint.
-   si le système d’exploitation est Windows Vista ou Windows 7, le compte de l’utilisateur est un utilisateur Standard et le contrôle de compte d’utilisateur est désactivé.

Ces deux scénarios sont rares. Toutefois, le patcher doit avoir le manifeste qui requiert des droits d’administrateur, et il doit appeler [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin); Si cette fonction retourne la valeur FALSe, le message d’erreur « les droits d’administrateur sont requis » s’affiche.

Globalement, la méthode 1 est préférable pour les jeux qui n’ont besoin que de quelques correctifs sur leur durée de vie.

## <a name="games-that-require-frequent-patches"></a>Jeux nécessitant des correctifs fréquents

De nombreux jeux basés sur Internet s’améliorent en permanence et nécessitent généralement des correctifs normaux. Pour ces jeux, les correctifs peuvent être appliqués par utilisateur ou par ordinateur, comme indiqué dans les rubriques suivantes. D’autres solutions possibles incluent la modification de la liste de contrôle d’accès qui protège% SystemDrive% \\ Program Files ou la création d’un service personnalisé.

### <a name="method-3-install-per-user"></a>Méthode 3 : installer Per-User

Une approche recommandée et simple consiste à installer l’ensemble du jeu dans un sous-dossier par utilisateur du dossier de données d’application local, que vous pouvez trouver en appelant [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) avec CSIDL \_ local \_ AppData. un exemple de chemin d’accès est C : \\ Documents et Paramètres \\ nom d’utilisateur \\ Local Paramètres \\ Application Data \\ ExampleGame. Un tel emplacement permet à une application qui s’exécute avec des droits d’utilisateur standard de modifier directement les fichiers de jeu.

Toutefois, il y a un inconvénient à cette approche lorsqu’un ordinateur a plusieurs utilisateurs : chaque utilisateur dispose d’une copie du jeu installée, et les correctifs doivent être téléchargés et appliqués par chaque utilisateur. Cela gaspille non seulement l’espace disque et le temps des utilisateurs, mais également l’utilisation de la bande passante réseau pour le serveur qui fournit des correctifs. En outre, étant donné que toute application avec des droits d’utilisateur standard peut modifier le jeu, les exécutables de jeu sont moins protégés. Il revient au fabricant du jeu de décider si cela est acceptable ou non.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Méthode 4 : installer dans un emplacement de Per-Computer commun

une autre méthode consiste à installer les données de jeu non exécutables dans un sous-répertoire du chemin d’accès spécifié par [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL \_ COMMON \_ APPDATA. un exemple de chemin d’accès est C : \\ Documents et Paramètres \\ tous les utilisateurs données d' \\ Application \\ ExampleGame. Il s’agit d’un emplacement partagé pour tous les utilisateurs et il peut être modifié par les applications qui s’exécutent avec des droits d’utilisateur standard. Cette méthode réduit la nécessité de réappliquer les correctifs importants lorsque le jeu est lu à partir de plusieurs comptes. Les fichiers exécutables du jeu doivent être conservés dans% SystemDrive% \\ Program Files pour réduire le risque d’autres comptes sur le système. Les fichiers exécutables doivent vérifier l’intégrité du nouveau contenu dans le répertoire partagé, car cet emplacement peut être modifié par un programme ou une personne disposant de droits d’utilisateur standard. envisagez d’utiliser [**MapFileAndCheckSum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) pour calculer une somme de contrôle des fichiers.

cette méthode présente l’avantage de fonctionner également bien sur Windows XP et Windows Vista, et elle ne nécessite pas de droits d’administrateur.

### <a name="other-possibilities"></a>Autres possibilités

En dehors des méthodes déjà évoquées, il est également possible de modifier la liste de contrôle d’accès du dossier de jeu% SystemDrive% \\ Program Files \\ \\ lors de l’installation du jeu afin qu’un outil de mise à jour puisse écrire directement dans les fichiers du jeu, même s’il est exécuté avec des droits d’utilisateur standard. Bien que cela ne soit pas difficile, elle contourne la protection de sécurité offerte par le système aux fichiers du jeu et permet aux programmes malveillants de modifier le contenu de l’annuaire. Cela n’est pas recommandé et il est fortement recommandé d’utiliser à la place une alternative.

Une dernière possibilité consiste à écrire un service personnalisé. En règle générale, l’écriture d’un service personnalisé pour corriger les jeux n’est pas une bonne idée, car cette action est compliquée et sujette aux erreurs. Il est recommandé d’appliquer les correctifs à l’aide d’autres méthodes décrites dans cet article. Toutefois, un service personnalisé peut être nécessaire lorsqu’il est combiné à des solutions anti-fraude ou anti-piratage. Un tel service doit prendre en charge un grand nombre de jeux et être conçu de façon à ce qu’il ne puisse télécharger les fichiers de correctifs et écrire que dans le répertoire d’installation du jeu cible. Il est important que le service soit de petite taille, ait une surface d’exposition minimale vulnérable aux attaques et utilise le moins de ressources système possible lorsque le jeu n’est pas en cours d’exécution.

## <a name="summary"></a>Résumé

Au final, c’est à vous de décider quelle méthode mettre en œuvre. Vous devez peser les facteurs qui sont importants pour vous. La sécurité, la fréquence des mises à jour correctives, la facilité d’utilisation par le client, la charge de travail nécessaire pour implémenter, la complexité de la solution et la conformité des fonctionnalités de la plateforme sont les facteurs que chaque développeur doit prendre en compte avant de décider d’une méthode particulière.

vous trouverez plus d’informations sur la protection des comptes d’utilisateur dans [Windows exigences de développement d’applications Vista pour le contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905330(v=msdn.10)).

 

 