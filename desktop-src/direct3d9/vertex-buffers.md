---
description: Les mémoires tampons de vertex, représentées par l’interface IDirect3DVertexBuffer9, sont des mémoires tampons qui contiennent des données de vertex.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Mémoires tampons de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e38feb34e7b9f637f383bf451bff812d9ee6fb1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746109"
---
# <a name="vertex-buffers-direct3d-9"></a>Mémoires tampons de vertex (Direct3D 9)

Les mémoires tampons de vertex, représentées par l’interface [**IDirect3DVertexBuffer9**](/windows/desktop/api) , sont des mémoires tampons qui contiennent des données de vertex. Les mémoires tampons de vertex peuvent contenir tout type de vertex transformé ou non transformé, éclairé ou non éclairé pouvant être rendu à l’aide des méthodes de rendu de l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Vous pouvez traiter les vertex dans une mémoire tampon de vertex pour effectuer des opérations telles que la transformation, l’éclairage ou la génération d’indicateurs de découpage. La transformation est toujours effectuée.

La flexibilité des mémoires tampons de vertex les rend idéales pour réutiliser la géométrie transformée. Vous pouvez créer une seule mémoire tampon de vertex, transformer, éclairer et découper les vertex dans celle-ci, et restituer le modèle dans la scène autant de fois que nécessaire sans le reconvertir, même avec des modifications d’état de rendu entrelacées. Cela est utile lors du rendu des modèles qui utilisent plusieurs textures : la géométrie est transformée une seule fois, puis des parties de celle-ci peuvent être rendues si nécessaire, entrelacées avec les modifications de texture requises. Les modifications de l’état de rendu effectuées après le traitement des vertex prennent effet lors du prochain traitement des vertex.

-   [Description](#description)
-   [Pool de mémoire et utilisation](#memory-pool-and-usage)

## <a name="description"></a>Description

Une mémoire tampon de vertex est décrite en termes de fonctionnalités : si elle peut exister uniquement dans la mémoire système, si elle est utilisée uniquement pour les opérations d’écriture, et le type et le nombre de vertex qu’elle peut contenir. Toutes ces caractéristiques sont conservées dans une structure [**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md) .

Le membre de format est défini sur D3DFMT \_ VERTEXDATA pour indiquer qu’il s’agit d’une mémoire tampon de vertex. Le type identifie le type de ressource de la mémoire tampon de vertex. Le membre de la structure d’utilisation contient des indicateurs de capacité généraux. L' \_ indicateur D3DUSAGE SOFTWAREPROCESSING indique que la mémoire tampon de vertex doit être utilisée avec le traitement du vertex logiciel. La présence de l' \_ indicateur WRITEONLY D3DUSAGE dans usage indique que la mémoire tampon de vertex est utilisée uniquement pour les opérations d’écriture. Cela libère le pilote pour placer les données de vertex dans le meilleur emplacement de mémoire pour permettre un traitement et un rendu rapides. Si l' \_ indicateur WRITEONLY D3DUSAGE n’est pas utilisé, le pilote est moins susceptible de placer les données dans un emplacement qui est inefficace pour les opérations de lecture. Cela sacrifie la vitesse de traitement et de rendu. Si cet indicateur n’est pas spécifié, il est supposé que les applications effectuent des opérations de lecture et d’écriture sur les données dans la mémoire tampon de vertex.

Pool spécifie la classe de mémoire allouée pour la mémoire tampon de vertex. L' \_ indicateur D3DPOOL SYSTEMMEM indique que le système a créé la mémoire tampon de vertex dans la mémoire système.

Le membre de taille stocke la taille, en octets, des données de mémoire tampon de vertex. Le membre de la Commission du prix final contient une combinaison de [D3DFVF](d3dfvf.md) qui identifient le type de vertex que contient la mémoire tampon.

## <a name="memory-pool-and-usage"></a>Pool de mémoire et utilisation

Vous pouvez créer des mémoires tampons de vertex avec la méthode [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/desktop/api) , qui prend le pool (classe de mémoire) et les paramètres d’utilisation. **IDirect3DDevice9 :: CreateVertexBuffer** peut également être créé avec un code de Commission de la Commission spécifié pour une utilisation dans le traitement de vertex de fonction fixe, ou comme sortie de vertex de processus. Pour plus d’informations, consultez la rubrique sur les [mémoires tampons de vertex (Direct3D 9)](fvf-vertex-buffers.md).

L' \_ indicateur D3DUSAGE SOFTWAREPROCESSING peut être défini lorsque le traitement en mode mixte ou le traitement du vertex logiciel (D3DCREATE \_ Mixed \_ VERTEXPROCESSING/D3DCREATE \_ Software \_ VERTEXPROCESSING) est activé pour cet appareil. D3DUSAGE \_ SOFTWAREPROCESSING doit être défini pour les mémoires tampons à utiliser avec le traitement du vertex logiciel en mode mixte, mais il ne doit pas être défini pour obtenir les meilleures performances possibles lors de l’utilisation du traitement des vertex matériels en mode mixte. ( D3DCREATE \_ matériel \_ VERTEXPROCESSING). Toutefois, la définition de D3DUSAGE \_ SOFTWAREPROCESSING est la seule option lorsqu’une seule mémoire tampon doit être utilisée avec le traitement du vertex matériel et logiciel. D3DUSAGE \_ SOFTWAREPROCESSING est autorisé pour les appareils mixtes et pour les périphériques logiciels.

Il est possible de forcer des tampons de vertex et d’index dans la mémoire système en spécifiant D3DPOOL \_ SYSTEMMEM, même lorsque le traitement du vertex est effectué dans le matériel. Il s’agit d’un moyen d’éviter une trop grande quantité de mémoire verrouillée en mode page lorsqu’un pilote met ces mémoires tampon dans la mémoire AGP.

Cette section présente les concepts nécessaires pour comprendre et utiliser des mémoires tampons de vertex dans une application Direct3D. Les informations sont réparties dans les sections suivantes.

-   [Création d’une mémoire tampon de vertex (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Accès au contenu d’une mémoire tampon de vertex (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Rendu à partir d’une mémoire tampon de vertex (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [Mémoires tampons de vertex du prix final (Direct3D 9)](fvf-vertex-buffers.md)
-   [Résolution du traitement des vertex de fonction (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Traitement de vertex programmable (Direct3D 9)](programmable-vertex-processing.md)
-   [Types d’appareils et exigences de traitement des vertex (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources Direct3D](direct3d-resources.md)
</dt> <dt>

[Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Mémoires tampons d’index (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
