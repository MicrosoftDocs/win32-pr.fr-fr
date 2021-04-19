---
title: Détection du lecteur Windows Media à partir d’une application
description: Détection du lecteur Windows Media à partir d’une application
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Lecteur Windows Media, détection à partir d’applications
- détection de Windows Media Player à partir d’applications
- Registre, détection de Windows Media Player à partir d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511451"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Détection du lecteur Windows Media à partir d’une application

Vous pouvez déterminer quelle version du lecteur Windows Media est installée en vérifiant la clé de Registre suivante :

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Active Setup \\ Components installée**

Pour le lecteur Windows Media 6,4, consultez la clé **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

Pour Windows Media Player 7 ou version ultérieure, consultez la clé **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.

Sous l’une de ces clés, si **isInstalled**<dl> <dt>

Type de données
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Type de données
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Redistribution du logiciel Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




