---
description: Lorsque le client a terminé la communication avec un serveur ou a terminé d’utiliser les informations d’identification supplémentaires transmises à la fonction AcquireCredentialsHandle, le client doit appeler la fonction FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Fin d’une session SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237924"
---
# <a name="ending-an-sspi-session"></a>Fin d’une session SSPI

Une fois que le client et le serveur ont terminé la communication, les deux côtés appellent la fonction [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) avec leurs handles de contexte respectifs. Lorsque le client a terminé la communication avec un serveur ou a terminé d’utiliser les informations d’identification supplémentaires transmises à la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , le client doit appeler la fonction [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) . Quand le serveur est prêt à être arrêté et avant de décharger la DLL, le serveur doit appeler **DeleteSecurityContext**.

 

 
