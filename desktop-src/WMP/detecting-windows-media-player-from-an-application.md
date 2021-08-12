---
title: détection des Lecteur Windows Media à partir d’une Application
description: détection des Lecteur Windows Media à partir d’une Application
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Lecteur Windows Media, détection à partir d’applications
- détection des Lecteur Windows Media à partir d’applications
- registre, détection de Lecteur Windows Media à partir d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267dc6c3202d9ecf894377899dfb34cf02ad42dfee05f8d42896c39ae48fc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579485"
---
# <a name="detecting-windows-media-player-from-an-application"></a>détection des Lecteur Windows Media à partir d’une Application

vous pouvez déterminer la version de Lecteur Windows Media installée en vérifiant la clé de registre suivante :

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Active Setup \\ Components installée**

pour Lecteur Windows Media 6,4, consultez la clé **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

pour plus d’Lecteur Windows Media 7 ou version ultérieure, consultez la clé **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.

Sous l’une de ces clés, si **isInstalled**<dl> <dt>

Type de données
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Type de données
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**redistribution du logiciel Lecteur Windows Media**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




