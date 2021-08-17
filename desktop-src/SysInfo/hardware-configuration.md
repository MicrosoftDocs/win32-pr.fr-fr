---
description: Les fonctions de configuration matérielle récupèrent des informations telles que le processeur, le profil matériel et les informations de clavier.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Hardware Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e396b2d08b489e92c7a407ca892250135fdd3d174d16de50d0c2d75428a88dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764417"
---
# <a name="hardware-configuration"></a>Hardware Configuration

Les fonctions de configuration matérielle récupèrent des informations telles que le processeur, le profil matériel et les informations de clavier.

La fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) récupère les informations sur le processeur et la mémoire, telles que la taille de la page, l’identificateur OEM (Original Equipment Manufacturer), le nombre et le type de processeurs, la plage d’adresses d’application, etc. La fonction [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) récupère des informations sur les opérations à virgule flottante et les jeux d’instructions pris en charge par le processeur.

La fonction [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) récupère des informations sur le profil matériel. Le profil matériel comprend des informations telles que l’état d’ancrage, l’identificateur global unique (GUID) et le nom d’affichage du profil. La fonction [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) récupère des informations telles que le type de clavier et le nombre de touches de fonction sur le clavier actuel.

 

 
