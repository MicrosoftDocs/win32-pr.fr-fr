---
description: Utilisation des cibles de rendu Direct3D
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Utilisation des cibles de rendu Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8aca19082c5db9521cfc1c7341fd74c98270cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524518"
---
# <a name="working-with-direct3d-render-targets"></a>Utilisation des cibles de rendu Direct3D

Plusieurs sous-types de média pour les cibles de rendu Direct3D sont définis pour être utilisés avec VMR-7 et VMR-9. Lorsqu’un filtre en amont propose une connexion avec l’un de ces sous-types, il indique à VMR que le rendu doit être effectué sur une cible de rendu Direct3D. Pour VMR-7, il s’agit d’une cible de rendu Direct3D DirectX 7, et pour VMR-9, il s’agit d’une cible de rendu Direct3D DirectX 9. Si VMR est en mode de mixage, la surface est également une surface de texture Direct3D. Si VMR n’est pas en mode de mixage, la surface sera une surface Direct3D normale. Les formats de pixel ARVB sont pris en charge uniquement lorsque VMR est en mode de mixage. Les sous-types de cibles de rendu sont les suivants :



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ virtuel DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ virtuel DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ virtuel DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ virtuel DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ virtuel DX9 \_ RT |



 

Ces types sont définis dans le fichier d’en-tête UUID. h. Les \_ types de média MEDIASUBTYPE RGB32 sont un format RGBx888 et les \_ types de média RGB16 MEDIASUBTYPE sont un format RGB565. Pour plus d’informations sur ces formats de pixels, consultez la documentation de DirectX Graphics.

**Demande d’une surface déverrouillée**

Le verrouillage et le déverrouillage des surfaces DirectDraw sont des opérations de calcul coûteuses. Lorsque vous utilisez les sous-types de médias de la cible de rendu Direct3D, le filtre amont a besoin que les surfaces soient déverrouillées pour pouvoir fonctionner dessus avec le matériel graphique. Pour éviter une opération de déverrouillage de verrouillage inutile, VMR prend en charge un nouvel indicateur sur la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , AM \_ GBF \_ NODDSURFACELOCK, qui indique à VMR de ne pas verrouiller la surface DirectDraw avant de passer un exemple au filtre amont. Lorsque cet indicateur est utilisé, les appels à [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) échouent, car il n’y a aucun pointeur verrouillé. Pour obtenir l’accès à la surface DirectDraw, le filtre doit appeler **QueryInterface** sur l’objet [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) retourné et demander l’interface [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Évidemment, le filtre amont doit s’assurer que la surface n’est pas verrouillée lorsqu’il rétablit l’échantillon dans la liste libre.

 

 



