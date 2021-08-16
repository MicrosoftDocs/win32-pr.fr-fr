---
description: Si vous écrivez un GINA pour remplacer la DLL GINA (MSGina.dll) standard de Microsoft, vous pouvez fournir une partie ou la totalité des fonctionnalités GINA standard.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: Fonctionnalités de MSGina.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf5d1e7e9dccf9581b27ea2fef3deb1c2c8aa218a1b0a711b7015134e1d2d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786748"
---
# <a name="msginadll-features"></a>Fonctionnalités de MSGina.dll

Si vous écrivez un [*Gina*](../secgloss/g-gly.md) pour remplacer la dll gina (MSGina.dll) standard de Microsoft, vous pouvez fournir une partie ou la totalité des fonctionnalités Gina standard. Voici une liste de fonctionnalités standard et une brève description de leur mode de contrôle.

> [!Note]  
> les dll GINA sont ignorées dans Windows Vista.

 

Les valeurs de clé de Registre contrôlent la disponibilité ou le comportement de nombreuses fonctionnalités GINA standard. Sauf indication contraire, ces valeurs de clés appartiennent à la clé de Registre Winlogon et ont un type de valeur de la valeur de \[ reg \_ SZ \] . Le chemin d’accès réel de la clé [*Winlogon*](../secgloss/w-gly.md) est le suivant :

**\\HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon**

-   **Boîte de dialogue notification légale**

    Dans certains cas, il est légal pour toute personne ayant accès à une station de travail de se connecter et de commencer à travailler, sauf si un avis indique que le système est destiné uniquement aux utilisateurs autorisés. En outre, de nombreux utilisateurs souhaitent que les messages spécifiques à l’entreprise s’affichent avant la connexion normale. La norme GINA utilise deux valeurs de clé de Registre Winlogon pour permettre à un système d’afficher des informations avant l’ouverture de session. Si l’une des valeurs de clé est présente et contient une chaîne non null, une boîte de dialogue d’avertissement légal s’affiche avant l’écran d’accueil habituel. Ces noms de valeur de clé sont présentés dans le tableau suivant.

    

    | Nom de la valeur de clé         | Contenu                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | Chaîne à afficher comme légende de la boîte de dialogue d’avertissement légal |
    | **LegalNoticeText**    | Chaîne à afficher comme message de la boîte de dialogue d’avertissement légal |

    

     

-   **Afficher le dernier nom d’utilisateur**

    Par défaut, l’écran de connexion affiche le nom du dernier utilisateur qui a réussi à se connecter à la station de travail. Cette fonctionnalité est contrôlée par la valeur de clé de Registre **DontDisplayLastUserName** . Lorsque cette valeur de clé est définie sur un, le nom d’utilisateur ne s’affiche pas dans la boîte de dialogue d’ouverture de session.

-   **Ouverture de session automatique**

    Cette fonctionnalité permet à un système de se connecter automatiquement à un utilisateur chaque fois que le système démarre en utilisant les informations par défaut et en désactivant la case à costar CTRL + ALT + SUPPR.

    Cette fonctionnalité utilise les valeurs suivantes de la clé Winlogon.

    

    | Valeur                 | Contenu                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | Nombre de fois où une ouverture de session automatique est en       |
    | **DefaultUserName**   | Nom du compte d’utilisateur                       |
    | **DefaultDomainName** | Nom du domaine dans lequel se trouve le compte d’utilisateur |

    

     

    Si la valeur de clé **AutoAdminLogon** est présente et contient une valeur et que la valeur de clé **AutoLogonCount** n’est pas présente, une ouverture de session automatique se produit chaque fois que l’utilisateur actuel ferme une session ou que le système est redémarré. Le compte en cours de connexion est spécifié à l’aide des valeurs de clé **DefaultUserName** et **DefaultDomainName** . Le mot de passe du compte peut être spécifié de deux façons. pour les ordinateurs exécutant l’un des systèmes d’exploitation Windows Server 2003 ou Windows XP, le mot de passe doit être stocké en tant que secret à l’aide de la fonction [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) . Pour plus d’informations, consultez [protection du mot de passe d’ouverture de session automatique](protecting-the-automatic-logon-password.md). L’autre façon de stocker le mot de passe est en texte brut dans l’entrée **DefaultPassword** de la clé Winlogon. pour des raisons de sécurité, cette technique doit être évitée. Si vous stockez le mot de passe à l’aide de la fonction **LsaStorePrivateData** , ne fournissez pas d’entrée **DefaultPassword** dans la clé Winlogon.

    Si la valeur de clé **AutoAdminLogon** est présente et contient une valeur, et si la valeur de clé **AutoLogonCount** est présente et n’est pas égale à zéro, **AutoLogonCount** détermine le nombre d’ouvertures de session automatiques qui se produisent. Chaque fois que le système est redémarré, la valeur de **AutoLogonCount** est décrémentée d’une unité, jusqu’à ce qu’elle atteigne zéro. Lorsque **AutoLogonCount** atteint zéro, aucun compte n’est connecté automatiquement, la valeur de clé **AutoLogonCount** et la valeur de clé **DefaultPassword** , si elle est utilisée, sont supprimées du Registre, et **AutoAdminLogon** est défini à zéro.

    L’utilisation de **AutoAdminLogon** présente un inconvénient supplémentaire : par défaut, MSGina.dll vérifie l’état de la touche Maj lorsque **AutoAdminLogon** en est un. Si la touche Maj est maintenue pendant le processus de démarrage, MSGina.dll ignore la valeur de clé **AutoAdminLogon** et invite l’utilisateur à entrer des informations d’identification et d’authentification de manière interactive. Il s’agit d’une fonctionnalité utile lorsque vous déboguez une application dédiée. Pour désactiver la signification de la touche Maj, définissez la valeur de clé **IgnoreShiftOverride** sur un.

-   **Autoriser l’arrêt non authentifié**

    Vous pouvez configurer le [*Gina*](../secgloss/g-gly.md) par défaut de façon à inclure un bouton **arrêter** dans la boîte de dialogue d’ouverture de session. Cela permet aux utilisateurs d’arrêter le système sans ouvrir de session préalable. La valeur de clé suivante détermine si ce bouton est inclus.

    

    | Valeur                    | Description                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Une pour inclure le bouton ; zéro pour exclure le bouton |

    

     

-   **ActivationUserinit.exe**

    Userinit.exe est une application exécutée par MSGina.dll lorsque l’utilisateur s’est connecté. Il s’exécute dans le [*contexte*](../secgloss/c-gly.md) de l’utilisateur qui vient d’être connecté et sur le Bureau de l’application. Son objectif est de configurer l’environnement de l’utilisateur, notamment la restauration des utilisations réseau, l’établissement de paramètres de profil tels que les polices et les couleurs d’écran, et l’exécution de scripts d’ouverture de session. Une fois ces tâches terminées, Userinit.exe exécute les programmes de l’interpréteur de commandes utilisateur. Les programmes de l’interpréteur de commandes héritent de l’environnement que Userinit.exe configure. Les programmes d’interpréteur de commandes spécifiques que Userinit.exe exécute sont stockés dans la valeur de clé de l' **interpréteur** de commandes sous la clé de Registre Winlogon.

    La valeur de clé de l' **interpréteur** de commandes peut contenir une liste de programmes séparés par des virgules à exécuter. Windows L’Explorateur est le programme d’interpréteur de commandes par défaut qui est exécuté si la valeur de la clé de l' **interpréteur** de commandes est nulle ou manquante. par défaut, Windows Explorer est listé.

-   **Options de sécurité connectées**

    Lorsque vous êtes connecté, si un utilisateur entre une [*séquence de touches*](../secgloss/s-gly.md) de sécurité (SAS), l’utilisateur reçoit un écran d’options de sécurité. Parmi les options répertoriées figurent :

    -   Arrêtez le système.
    -   Fermez la session.
    -   Modifiez le mot de passe.
    -   Accédez à la liste des tâches.
    -   Verrouillez la station de travail.

    Une GINA de remplacement peut fournir des options similaires lorsqu’un événement SAS est reçu lorsqu’un utilisateur a ouvert une session.

 

 
