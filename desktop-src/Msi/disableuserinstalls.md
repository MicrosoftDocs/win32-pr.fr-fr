---
description: Il s’agit d’une stratégie système par ordinateur qui peut être utilisée lorsque l’administrateur souhaite uniquement installer les applications par ordinateur.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112275"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Il s’agit d’une [stratégie système](system-policy.md) par ordinateur qui peut être utilisée lorsque l’administrateur souhaite uniquement installer les applications par ordinateur.

Si cette stratégie n’est pas définie, le programme d’installation recherche les applications dans le registre dans l’ordre suivant : applications gérées inscrites en tant qu’applications par utilisateur, applications non gérées inscrites en tant qu’utilisateur et enfin applications inscrites en tant qu’ordinateur.

Si cette stratégie est définie sur 1, le programme d’installation ignore toutes les applications inscrites en tant qu’utilisateur et recherche uniquement les applications inscrites en tant qu’ordinateur. Les appels à l’interface de programmation d’applications Windows Installer ou au système ignorent les applications par utilisateur. Si vous tentez d’effectuer une installation dans le [contexte d’installation](installation-context.md) par utilisateur, le programme d’installation affiche un message d’erreur et arrête l’installation. Dans ce cas, le Windows Installer empêche également les installations par utilisateur à partir d’un serveur Terminal Server.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



