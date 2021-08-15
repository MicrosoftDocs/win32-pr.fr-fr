---
description: ICE97 vérifie que deux composants n’isolent pas un composant partagé dans le même répertoire.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29575d533e945cef922110315cd3300f56fe62ae61b34c92de7175916e6657ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315239"
---
# <a name="ice97"></a>ICE97

ICE97 vérifie que deux composants n’isolent pas un composant partagé dans le même répertoire.

## <a name="result"></a>Résultat

ICE97 publie les avertissements suivants.



| AVERTISSEMENT ICE97                                                                                                                                                                    | Description                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Ce composant \[ 1 \] installe le composant partagé dans le même répertoire \[ 2 \] qu’un autre, ce qui interrompt les règles des composants si les deux composants (ou plus) sont sélectionnés pour l’installation. | Deux composants ne doivent pas isoler un composant partagé dans le même répertoire. |



 

Par exemple, Composant1 et COMPONENT2, qui partagent ComponentShared, sont installés dans le même répertoire. Les deux spécifient ComponentShared comme un composant isolé. En raison de l’isolation, les fichiers dans ComponentShared sont copiés deux fois dans la \_ référence de répertoire pour Composant1 et COMPONENT2. Les composants disposent désormais d’un nombre de références sur la copie des fichiers. Il s’agit d’une violation des règles du composant d’installation. Si Composant1 est désinstallé, les fichiers des composants isolés sont supprimés et COMPONENT2 est interrompu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



