---
description: La mémoire tampon de compatibilité est spécifique à la norme Q. 931 RNIS. Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Mémoire tampon de compatibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739063a6570a93b1fb05442ebe3f6ec10a040626ba7a0fe4b9692d7e5636b5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946591"
---
# <a name="compatibility-buffer"></a>Mémoire tampon de compatibilité

La mémoire tampon de compatibilité est spécifique à la norme Q. 931 RNIS. Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** et **dwLowLevelCompOffset** les membres de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIM \_ HIGHLEVELCOMPATIBILITYBUFFER** et **CIM \_ LOWLEVELCOMPATIBILITYBUFFER** membre de [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
