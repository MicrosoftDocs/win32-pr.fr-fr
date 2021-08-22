---
title: accès au contrôle à partir de Visual Basic et d’autres langages de programmation
description: accès au contrôle à partir de Visual Basic et d’autres langages de programmation
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fe0c5e7548283a84edff1fb3ded488c1367087e12c15d1578629ce80b51297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976859"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>accès au contrôle à partir de Visual Basic et d’autres langages de programmation

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

vous pouvez également utiliser le contrôle de Microsoft Agent à partir de Visual Basic et d’autres langages de programmation. assurez-vous que la langue prend entièrement en charge l’interface de contrôle ActiveX et suivez ses conventions pour ajouter des contrôles ActiveX et y accéder. Pour accéder au contrôle, l’agent doit déjà être installé sur le système cible.

Vous pouvez ensuite télécharger le fichier cab d’installation automatique de l’agent à partir du site Web (à l’aide de l’option Enregistrer au lieu de exécuter). Vous pouvez inclure ce fichier dans votre programme d’installation de. Chaque fois qu’il est exécuté, il installe automatiquement l’agent sur le système cible. Pour plus d’informations sur l’installation, consultez le contrat de licence de distribution Microsoft Agent. L’installation autre que l’utilisation du fichier cab à installation automatique de l’agent, telle que la tentative de copie et l’inscription des fichiers de composants de l’agent, n’est pas prise en charge. Cela garantit une installation cohérente et complète. notez que le fichier d’installation automatique de microsoft Agent ne s’installe pas sur microsoft Windows 2000, car cette version du système d’exploitation comprend déjà sa propre version de l’Agent.

pour installer correctement l’Agent sur un système cible, vous devez également vous assurer que le système cible dispose d’une version récente du Microsoft Visual C++ runtime (Msvcrt.dll), de l’outil d’inscription microsoft (Regsvr32.dll) et des dll microsoft COM. Le moyen le plus simple de s’assurer que les composants nécessaires se trouvent sur le système cible est d’exiger l’installation de Microsoft Internet Explorer 3,02 ou version ultérieure. Vous pouvez également installer les deux premiers composants qui sont disponibles dans le cadre de Microsoft Visual C++. Les DLL COM nécessaires peuvent être installées dans le cadre de la mise à jour Microsoft DCOM, disponible sur le site Web de Microsoft. Vous trouverez des informations supplémentaires et des informations de licence pour ces composants sur le site Web de Microsoft.

Les composants de langue de l’agent peuvent être installés de la même façon. De même, vous pouvez utiliser cette technique pour installer le format des services ACS des caractères Microsoft disponibles pour la distribution à partir du site Web de Microsoft Agent. Les fichiers de caractères sont automatiquement installés dans le \\ sous-répertoire Microsoft Agent chars.

Étant donné que les composants de Microsoft Agent sont conçus en tant que composants du système d’exploitation, l’agent n’est peut-être pas désinstallé. de même, lorsque l’agent est déjà installé dans le cadre du système d’exploitation Windows, le cabinet à installation automatique de l’agent peut ne pas s’installer.

 

 




