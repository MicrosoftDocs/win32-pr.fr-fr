---
title: Obtention d’un ordinateur SDO
description: La première étape de l’utilisation de l’API SDO consiste à créer un objet ordinateur SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031491"
---
# <a name="obtaining-a-machine-sdo"></a>Obtention d’un ordinateur SDO

La première étape de l’utilisation de l’API SDO consiste à créer un objet ordinateur SDO.

Utilisez la fonction [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) pour obtenir l’identificateur de classe (CLSID) de l’objet ordinateur SDO. L’identificateur programmatique (ProgID) à utiliser pour l’objet est «IAS. SdoMachine".

Une fois que vous avez le CLSID, appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec ce CLSID. Spécifiez [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) en tant qu’interface pour laquelle un pointeur doit être retourné.

Consultez [attachement à un ordinateur SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) pour obtenir un exemple de code qui montre comment obtenir un ordinateur SDO.

 

 