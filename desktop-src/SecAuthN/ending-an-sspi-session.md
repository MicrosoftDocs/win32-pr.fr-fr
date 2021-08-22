---
description: Lorsque le client a terminé la communication avec un serveur ou a terminé d’utiliser les informations d’identification supplémentaires transmises à la fonction AcquireCredentialsHandle, le client doit appeler la fonction FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Fin d’une session SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4669d3143b480df20f1a5f1d76e73cc75802766d1db83da9b75d304e256ae4dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008267"
---
# <a name="ending-an-sspi-session"></a>Fin d’une session SSPI

Une fois que le client et le serveur ont terminé la communication, les deux côtés appellent la fonction [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) avec leurs handles de contexte respectifs. Lorsque le client a terminé la communication avec un serveur ou a terminé d’utiliser les informations d’identification supplémentaires transmises à la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , le client doit appeler la fonction [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) . Quand le serveur est prêt à être arrêté et avant de décharger la DLL, le serveur doit appeler **DeleteSecurityContext**.

 

 
