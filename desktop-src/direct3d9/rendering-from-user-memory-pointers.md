---
description: Un ensemble secondaire d’interfaces de rendu prend en charge la transmission de données de vertex et d’index directement à partir de pointeurs de mémoire utilisateur. Ces interfaces ne prennent en charge qu’un seul flux de données de vertex. Pour plus d’informations, consultez les rubriques de référence suivantes.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Rendu à partir de pointeurs de mémoire utilisateur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9893d3728b3bac8bc38dd8118f995510de834d2c6e54cdadcafe2c26b8a78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746479"
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

 

 
