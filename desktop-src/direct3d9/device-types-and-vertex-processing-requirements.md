---
description: Les performances des opérations de traitement des vertex, y compris la transformation et l’éclairage, dépendent fortement de l’emplacement de la mémoire tampon de vertex dans la mémoire et du type de périphérique de rendu utilisé.
ms.assetid: 4f9ca83d-c9d6-4749-944d-78f831b0f44e
title: Types d’appareils et exigences de traitement des vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9c74e538c9a5b5298fffbd86492c67e2332e4013485c8849d66021234fdbb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044457"
---
# <a name="device-types-and-vertex-processing-requirements-direct3d-9"></a>Types d’appareils et exigences de traitement des vertex (Direct3D 9)

Les performances des opérations de traitement des vertex, y compris la transformation et l’éclairage, dépendent fortement de l’emplacement de la mémoire tampon de vertex dans la mémoire et du type de périphérique de rendu utilisé. Les applications contrôlent l’allocation de mémoire pour les mémoires tampons de vertex lorsqu’elles sont créées. Lorsque l' \_ indicateur de mémoire D3DPOOL SYSTEMMEM est défini, la mémoire tampon de vertex est créée dans la mémoire système. Lorsque l' \_ indicateur de mémoire par défaut D3DPOOL est utilisé, le pilote de périphérique détermine l’emplacement de la mémoire pour la mémoire tampon de vertex, souvent appelée mémoire optimale pour le pilote. La mémoire optimale pour le pilote peut être une mémoire vidéo locale, une mémoire vidéo non locale ou une mémoire système.

La définition de la \_ constante D3DUSAGE SOFTWAREPROCESSING avec [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) active le traitement du vertex logiciel sur les données de la mémoire tampon du vertex. Cet indicateur est requis pour le traitement des vertex logiciels en mode mixte. L’indicateur ne peut pas être utilisé pour le mode de traitement du vertex matériel. Les mémoires tampons de vertex utilisées avec le traitement du vertex logiciel sont les suivantes :

-   Tous les flux d’entrée pour [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).
-   Tous les flux d’entrée pour [**IDirect3DDevice9 ::D rawprimitive**](/windows/desktop/api) et [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Le raisonnement que vous utilisez pour déterminer l’emplacement de la mémoire-système ou pilote optimal pour les mémoires tampons de vertex est le même que pour les textures. Le traitement des vertex, y compris la transformation et l’éclairage, dans le matériel fonctionne mieux lorsque les tampons de vertex sont alloués dans la mémoire optimale du pilote, tandis que le traitement du vertex logiciel fonctionne mieux avec les mémoires tampons de vertex allouées dans la mémoire système. Pour les textures, la pixellisation matérielle fonctionne mieux lorsque les textures sont allouées dans la mémoire optimale du pilote, tandis que la pixellisation des logiciels fonctionne mieux avec les textures de mémoire système.

Microsoft Direct3D 9 prend en charge le traitement autonome des vertex, sans rendu de primitive avec la méthode [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) . Ce traitement de vertex autonome est toujours effectué dans le logiciel sur le processeur hôte. Pour cette raison, les mémoires tampons de vertex utilisées comme sources définies avec [**IDirect3DDevice9 :: SetStreamSource**](/windows/desktop/api) doivent être créées avec l' \_ indicateur SOFTWAREPROCESSING D3DUSAGE. La fonctionnalité fournie par **IDirect3DDevice9 ::P rocessvertices** est identique à celle des méthodes [**IDirect3DDevice9 ::D rawprimitive**](/windows/desktop/api) et [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) lors de l’utilisation du traitement du vertex logiciel.

Si votre application effectue son propre traitement de vertex et passe des sommets transformés, allumés et découpés aux méthodes de rendu, l’application peut écrire directement des vertex dans une mémoire tampon de vertex allouée dans la mémoire optimale du pilote. Cette technique empêche ultérieurement une opération de copie redondante. Notez que cette technique ne fonctionne pas correctement si votre application lit les données à partir d’une mémoire tampon de vertex, car les opérations de lecture effectuées par l’hôte à partir de la mémoire optimale du pilote peuvent être très lentes. Par conséquent, si votre application doit lire au cours du traitement ou écrire des données dans la mémoire tampon de façon erratique, une mémoire tampon de vertex de mémoire système est un meilleur choix.

Lors de l’utilisation des fonctionnalités de traitement du vertex Direct3D (en passant des vertex non transformés aux méthodes de rendu de la mémoire tampon de vertex), le traitement peut avoir lieu sur le matériel ou les logiciels selon le type d’appareil et les indicateurs de création de périphérique. Il est recommandé d’allouer des tampons de vertex dans le pool D3DPOOL \_ par défaut pour des performances optimales dans presque tous les cas. Lorsqu’un appareil utilise le traitement du vertex matériel, il existe un certain nombre d’optimisations supplémentaires qui peuvent être effectuées en fonction des indicateurs D3DUSAGE \_ dynamique et D3DUSAGE \_ WRITEONLY. Pour plus d’informations sur l’utilisation de ces indicateurs, consultez IDirect3DDevice9 :: CreateVertexBuffer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de vertex](vertex-buffers.md)
</dt> </dl>

 

 
