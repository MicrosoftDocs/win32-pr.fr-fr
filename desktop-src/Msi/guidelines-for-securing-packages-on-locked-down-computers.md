---
description: Pour aider à maintenir une installation logicielle sécurisée sur des ordinateurs verrouillés, respectez ces instructions lors de la création du package Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Sécurisation des packages sur les ordinateurs verrouillés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866314"
---
# <a name="securing-packages-on-locked-down-computers"></a><span data-ttu-id="f6da4-103">Sécurisation des packages sur les ordinateurs verrouillés</span><span class="sxs-lookup"><span data-stu-id="f6da4-103">Securing Packages on Locked-Down Computers</span></span>

<span data-ttu-id="f6da4-104">Lorsque vous créez un package Windows Installer qui sera utilisé sur des ordinateurs verrouillés, vous respectez les instructions suivantes pour assurer la maintenance d’un environnement sécurisé lors de l’installation :</span><span class="sxs-lookup"><span data-stu-id="f6da4-104">Adherence to the following guidelines when authoring a Windows Installer package that will be used on locked-down computers helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="f6da4-105">Testez la compatibilité de votre package avec la [stratégie système](system-policy.md)de l’ordinateur Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f6da4-105">Test your package for compatibility with the Windows Installer machine [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="f6da4-106">Veillez à ce que le package s’exécute avec tous les [niveaux d’interface utilisateur](user-interface-levels.md), aucun, de base, limité et complet.</span><span class="sxs-lookup"><span data-stu-id="f6da4-106">Make sure you package runs with all [user interface levels](user-interface-levels.md), none, basic, limited, and full.</span></span>
-   <span data-ttu-id="f6da4-107">Testez votre package sur des partitions NTFS, avec des privilèges [*élevés*](e-gly.md) et non élevés.</span><span class="sxs-lookup"><span data-stu-id="f6da4-107">Test your package on NTFS partitions, both with [*elevated*](e-gly.md) and non-elevated privileges.</span></span>
-   <span data-ttu-id="f6da4-108">À compter de Windows Installer 3,0, la mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md) permet aux utilisateurs non-administrateurs d’appliquer des correctifs aux applications installées dans le contexte par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f6da4-108">Starting with Windows Installer 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="f6da4-109">Testez votre package de correctifs sur Windows Vista et Windows XP pour l’installation par les utilisateurs disposant d’un accès administrateur et par des utilisateurs non-administrateurs.</span><span class="sxs-lookup"><span data-stu-id="f6da4-109">Test your patch package on Windows Vista and Windows XP for both installation by users with administrator access and by non-administrator users.</span></span>

 

 



