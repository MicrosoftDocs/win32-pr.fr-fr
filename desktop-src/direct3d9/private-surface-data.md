---
description: Vous pouvez stocker n’importe quel type de données spécifiques à l’application à l’aide d’une surface. Par exemple, une surface représentant une carte dans un jeu peut contenir des informations sur le terrain.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Données de surface privée (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515333"
---
# <a name="private-surface-data-direct3d-9"></a>Données de surface privée (Direct3D 9)

Vous pouvez stocker n’importe quel type de données spécifiques à l’application à l’aide d’une surface. Par exemple, une surface représentant une carte dans un jeu peut contenir des informations sur le terrain.

Une surface peut avoir plusieurs mémoires tampons de données privées. Chaque mémoire tampon est identifiée par un GUID que vous fournissez lors de l’attachement des données à l’aire de conception.

Pour stocker des données de surface privée, utilisez SetPrivateData, en passant un pointeur vers la mémoire tampon source, la taille des données et un GUID défini par l’application pour les données. Éventuellement, les données sources peuvent exister sous la forme d’un objet COM ; dans ce cas, vous transmettez un pointeur vers le pointeur d’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’objet et vous définissez l' \_ indicateur D3DSPD IUNKNOWNPOINTER.

SetPrivateData alloue une mémoire tampon interne pour les données et la copie. Vous pouvez ensuite libérer en toute sécurité l’objet ou la mémoire tampon source. La mémoire tampon interne ou la référence d’interface est libérée lorsque FreePrivateData est appelé. Cela se produit automatiquement lorsque la surface est libérée.

Pour récupérer des données privées pour une surface, vous devez allouer une mémoire tampon de la taille correcte, puis appeler la méthode GetPrivateData, en passant le GUID qui a été assigné aux données. Vous êtes responsable de la libération de la mémoire dynamique que vous utilisez pour cette mémoire tampon. Si les données sont un objet COM, cette méthode récupère le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

Si vous ne connaissez pas la taille de la mémoire tampon à allouer, appelez d’abord GetPrivateData avec zéro dans pSizeOfData. Si la méthode échoue avec D3DERR \_ MOREDATA, elle retourne le nombre d’octets nécessaires pour la mémoire tampon.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
