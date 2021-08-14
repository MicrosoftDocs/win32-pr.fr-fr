---
title: Limite de temps
description: Limite de temps
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- CAPTUREPARMS, structure
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- CAPTUREPARMS, structure
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6211edf3ce3fb86b4c0430c685ff05ff7f95c718c0a89e7ba782ae342feb18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801263"
---
# <a name="time-limit"></a>Limite de temps

Vous pouvez limiter la durée d’une opération de capture à l’aide des membres **fLimitEnabled** et **wTimeLimit** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Le membre **fLimitEnabled** indique si l’opération de capture doit être chronométrée, tandis que **wTimeLimit** spécifie la durée maximale de l’opération de capture.

Vous pouvez récupérer les valeurs de **fLimitEnabled** et **wTimeLimit** à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de la limite WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Vous pouvez activer un minuteur pour l’opération de capture en spécifiant **true** comme valeur de **fLimitEnabled**, ou vous pouvez définir la durée de l’opération de capture en spécifiant une valeur, en secondes, pour **wTimeLimit**. Après avoir défini ces membres, envoyez la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). La valeur par défaut de **fLimitEnabled** est **false**.

 

 




