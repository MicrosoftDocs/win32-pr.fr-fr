---
description: étant donné que le contrôle de compte d’utilisateur (UAC) dans Windows Vista limite les privilèges au cours d’une installation, les développeurs de Windows Installer packages ne doivent pas supposer que leur installation a toujours accès à toutes les parties du système.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Instructions pour les packages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db228c2dff443d421ddc089074f0fcce6ae93e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021667"
---
# <a name="guidelines-for-packages"></a>Instructions pour les packages

étant donné que [*le contrôle de compte d’utilisateur*](u-gly.md) (UAC) dans Windows Vista limite les privilèges au cours d’une installation, les développeurs de Windows Installer packages ne doivent pas supposer que leur installation a toujours accès à toutes les parties du système.

dans la plupart des cas, un package d’installation qui peut être déployé pour les utilisateurs standard via [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page) doit également fonctionner avec le contrôle de compte d’utilisateur dans Windows Vista. Des exceptions peuvent se produire si la [table InstallUISequence](installuisequence-table.md) contient l' [action LaunchConditions](launchconditions-action.md) ou si la [table LaunchCondition](launchcondition-table.md) contient une condition basée sur la [propriété Privileged](privileged.md). Windows les développeurs de packages d’installation doivent donc respecter les consignes suivantes pour s’assurer que leur package fonctionne avec le contrôle de compte d’utilisateur et Windows Vista.

-   Quand vous incluez une condition de [*contexte d’installation*](i-gly.md) avec une action dans la [table InstallUISequence](installuisequence-table.md), utilisez une instruction conditionnelle basée sur la [propriété Privileged](privileged.md). N’utilisez pas de condition basée sur la propriété [**adminuser**](adminuser.md) .
-   Lorsque vous incluez le contexte d’installation avec les conditions de lancement de l’installation, utilisez une [action personnalisée de type 19](custom-action-type-19.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md) et faites en sorte que l’action personnalisée soit subordonnée à la [propriété Privileged](privileged.md). N’utilisez pas d’action dans la [table LaunchCondition](launchcondition-table.md) avec une condition basée sur la [propriété adminuser](adminuser.md) ou la propriété Privileged.
-   Pour lire ou modifier la configuration du système, utilisez une [action personnalisée d’exécution différée](deferred-execution-custom-actions.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md). N’utilisez pas d’actions personnalisées d’exécution immédiate dans la [table InstallUISequence](installuisequence-table.md) pour modifier la configuration du système.
-   Pour modifier des parties du système qui ne sont pas spécifiques à l’utilisateur, utilisez une action personnalisée différée dans la [table InstallExecuteSequence](installexecutesequence-table.md). Vous devez inclure le bit msidbCustomActionTypeNoImpersonate dans le type d’action personnalisé.
-   Omettez le bit 3 de la valeur de la propriété Résumé du [**nombre de mots**](word-count-summary.md) pour indiquer que le package peut être nécessaire pour être élevé. N’incluez pas ce bit, sauf si des privilèges élevés ne sont pas nécessaires pour installer ce package.
-   Incluez un manifeste avec le niveau d’exécution demandé de l’application.
-   Incluez un certificat dans la table [MsiPatchCertificate](msipatchcertificate-table.md) du package d’origine et signez tous les correctifs avec le même certificat.
-   si des privilèges élevés sont requis pour installer un package Windows Installer, l’auteur du package doit inclure l’attribut [ElevationShield](elevationshield-attribute.md) pour le [contrôle PushButton](pushbutton-control.md) utilisé pour démarrer l’installation. Cela permet d’avertir l’utilisateur que cliquer sur le bouton affiche la boîte de dialogue UAC demandant l’autorisation de l’administrateur pour poursuivre l’installation.
-   affectez à la propriété [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) la valeur 1 pour indiquer au Windows Installer que le package a été créé et testé pour se conformer au contrôle de compte d’utilisateur dans Windows Vista. Si cette propriété n’est pas définie, le programme d’installation détermine si le package est conforme au contrôle de compte d’utilisateur.

en dehors de [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page), la vérification suivante de la conformité UAC peut être utilisée sur Windows XP.

**Pour vérifier la conformité du contrôle de compte d’utilisateur en dehors de stratégie de groupe**

1.  Connectez-vous à l’ordinateur en tant qu’administrateur.
2.  Publiez le package pour une installation par ordinateur :

    *package.msi* **msiexec/JM**

3.  Fermez la session sur l’ordinateur.
4.  Connectez-vous à l’ordinateur en tant qu’utilisateur standard.
5.  Tentative d’installation du package publié :

    **msiexec/i** *package.msi*

6.  Dans la plupart des cas, si l’installation réussit, le package est conforme au contrôle de compte d’utilisateur.
7.  Affectez la valeur 1 à la propriété [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) dans le package.
8.  testez l’installation correcte du package à l’aide de Windows Vista.

 

 
