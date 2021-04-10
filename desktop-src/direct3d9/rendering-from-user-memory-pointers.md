---
description: Un ensemble secondaire d’interfaces de rendu prend en charge la transmission de données de vertex et d’index directement à partir de pointeurs de mémoire utilisateur. Ces interfaces ne prennent en charge qu’un seul flux de données de vertex. Pour plus d’informations, consultez les rubriques de référence suivantes.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Rendu à partir de pointeurs de mémoire utilisateur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200777"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a>Rendu à partir de pointeurs de mémoire utilisateur (Direct3D 9)

Un ensemble secondaire d’interfaces de rendu prend en charge la transmission de données de vertex et d’index directement à partir de pointeurs de mémoire utilisateur. Ces interfaces ne prennent en charge qu’un seul flux de données de vertex. Pour plus d’informations, consultez les rubriques de référence suivantes.

-   [**IDirect3DDevice9 ::D rawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [**IDirect3DDevice9 ::D rawIndexedPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

Ces méthodes s’affichent avec les données spécifiées par les pointeurs de mémoire utilisateur, au lieu des mémoires tampons de vertex et d’index.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu des primitives](rendering-primitives.md)
</dt> </dl>

 

 
