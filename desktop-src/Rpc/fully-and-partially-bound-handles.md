---
title: Handles entièrement et partiellement liés
description: Lorsque vous utilisez des points de terminaison dynamiques, les bibliothèques Runtime obtiennent les informations de point de terminaison telles qu’elles en ont besoin.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311506"
---
# <a name="fully-and-partially-bound-handles"></a>Handles entièrement et partiellement liés

Lorsque vous utilisez des points de terminaison dynamiques, les bibliothèques Runtime obtiennent les informations de point de terminaison telles qu’elles en ont besoin. Les bibliothèques Runtime font la distinction entre un *handle entièrement lié* (un qui inclut des informations de point de terminaison) et un *handle partiellement lié* (un qui n’inclut pas d’informations de point de terminaison).

La bibliothèque Runtime cliente doit convertir le handle partiellement lié en un handle entièrement lié avant que le client puisse effectuer une liaison au serveur. La bibliothèque Runtime cliente tente de convertir le handle partiellement lié pour l’application cliente en obtenant les informations de point de terminaison comme indiqué :

-   À partir de la spécification de l’interface du client
-   À partir d’un service de mappage de point de terminaison s’exécutant sur le serveur

Si le client essaie d’utiliser un handle partiellement lié lorsque les informations de point de terminaison ne sont pas disponibles dans la spécification d’interface et que le mappeur de point de terminaison du serveur n’a pas d’informations sur le point de terminaison de serveur, le client ne disposera pas de suffisamment d’informations pour effectuer son appel de procédure distante et cet appel échouera. Pour éviter cela, vous devez inscrire le point de terminaison dans le mappeur de point de terminaison lorsque votre application distribuée utilise des handles partiellement liés. Pour plus d’informations sur le mappeur de point de terminaison, consultez [spécification de points de terminaison dynamiques](specifying-endpoints.md).

En cas d’échec d’un appel de procédure distante, l’application cliente peut appeler [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) pour supprimer les informations de point de terminaison obsolètes. Lorsque le client essaie d’appeler la procédure distante, la bibliothèque Runtime cliente tente à nouveau de convertir le handle entièrement lié en handle partiellement lié. Cela est utile lorsque le serveur a été arrêté et redémarré à l’aide d’un point de terminaison dynamique différent.

 

 




