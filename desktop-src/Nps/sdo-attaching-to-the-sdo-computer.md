---
title: Attachement à l’ordinateur SDO
description: Avec le pointeur d’interface retourné par CoCreateInstance, appelez la méthode d’attachement ISdoMachine.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941066"
---
# <a name="attaching-to-the-sdo-computer"></a>Attachement à l’ordinateur SDO

Avec le pointeur d’interface retourné par [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), appelez la méthode [**ISdoMachine :: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) . Passer **null** comme paramètre à la méthode **Attach** . La valeur **null** spécifie que **Attach** associe l’objet ordinateur à l’ordinateur local. L’attachement à un ordinateur distant n’est pas pris en charge.

Pour déterminer si l’ordinateur local est déjà attaché, appelez la méthode [**ISdoMachine :: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .

Consultez [attachement à un ordinateur SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) pour obtenir un exemple de code qui montre comment s’attacher à l’ordinateur local.

 

 