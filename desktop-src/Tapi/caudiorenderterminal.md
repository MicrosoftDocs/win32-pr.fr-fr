---
description: Le terminal CAudioRenderTerminal est dérivé de CSingleFilterTerminal et implémente un terminal de rendu audio statique pour les appareils Wave à l’aide du filtre DirectShow WaveOut. La plupart des MSP n’ont pas besoin de remplacer l’implémentation de ce terminal.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544970"
---
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

Le terminal **CAudioRenderTerminal** est dérivé de [CSingleFilterTerminal](csinglefilterterminal.md) et implémente un terminal de rendu audio statique pour les appareils Wave à l’aide du filtre DirectShow WaveOut. La plupart des MSP n’ont pas besoin de remplacer l’implémentation de ce terminal.

Défini dans MSPtrmar. h.

## <a name="remarks"></a>Notes

Les méthodes [**put \_ Solde**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) et [**obtenir l' \_ équilibre**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** ne sont pas implémentées et retournent E \_ NOTIMPL.

 

 



