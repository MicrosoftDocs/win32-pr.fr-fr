---
title: Lancement de l’utilisateur
description: Lancement de l’utilisateur
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293687"
---
# <a name="launching-user"></a>Lancement de l’utilisateur

Il s’agit du paramètre par défaut pour l’identité de l’application. Lorsque l’utilisateur de lancement est choisi pour l’identité de l’application, chaque compte client obtient une nouvelle instance du serveur et chaque serveur reçoit sa propre [station Windows](/windows/desktop/winstation/window-stations). En raison des instances de serveur distinctes, le lancement de l’utilisateur est le paramètre d’identité de protection de sécurité de niveau supérieur. Toutefois, il existe des limites limitées sur la consommation des ressources. En outre, toute interface utilisateur graphique affichée par le serveur n’est pas visible par le client.

Si l’application a l’identité de l’utilisateur de lancement, elle s’exécute avec un jeton d’emprunt d’identité. Pour plus d’informations sur l’emprunt d’identité et les jetons d’accès, consultez [niveaux d’emprunt d’identité](impersonation-levels.md) et [masquage](cloaking.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Identité de l'application](application-identity.md)
</dt> <dt>

[Utilisateur interactif](interactive-user.md)
</dt> <dt>

[Identité du service](service-identity.md)
</dt> <dt>

[Utilisateur spécifié](specified-user.md)
</dt> </dl>

 

 