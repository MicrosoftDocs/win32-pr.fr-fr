---
title: Signatures racines
description: La signature racine définit les types de ressources qui sont liés au pipeline Graphics.
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4c034e208dd841545777cc92878e7020b9b4a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548557"
---
# <a name="root-signatures"></a>Signatures racines

La signature racine définit les types de ressources qui sont liés au pipeline Graphics.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d’ensemble des signatures racines](root-signatures-overview.md)<br/>                                                 | Une signature racine est configurée par les listes de commandes App et Links pour les ressources requises par les nuanceurs. La liste de commandes Graphics comporte à la fois une signature de graphique et une signature racine de calcul. Une liste de commandes Compute aura simplement une signature racine de calcul. Ces signatures racines sont indépendantes les unes des autres.<br/>                                                                                             |
| [Utilisation d’une signature racine](using-a-root-signature.md)<br/>                                                     | La signature racine est la définition d’une collection de tables de descripteurs réorganisée arbitrairement (y compris leur disposition), de constantes racine et de descripteurs racine. Chaque entrée a un coût pour une limite maximale. par conséquent, l’application peut effectuer un compromis entre le nombre de chaque type d’entrée que la signature racine contiendra.<br/>                                                                     |
| [Création d’une signature racine](creating-a-root-signature.md)<br/>                                               | Les signatures racines sont une structure de données complexe contenant des structures imbriquées. Celles-ci peuvent être définies par programme à l’aide de la définition de la structure de données ci-dessous (qui comprend des méthodes pour aider à initialiser les membres). Elles peuvent également être créées dans le langage HLSL (High Level Shading Language), ce qui permet au compilateur de valider au préalable que la disposition est compatible avec le nuanceur. <br/> |
| [Limites de signature racine](root-signature-limits.md)<br/>                                                       | La signature racine est un grand patrimoine et il existe des limites et des coûts stricts à prendre en compte.<br/>                                                                                                                                                                                                                                                                                                            |
| [Utilisation des constantes directement dans la signature racine](using-constants-directly-in-the-root-signature.md)<br/>     | Les applications peuvent définir des constantes racine dans la signature racine, chacune sous la forme d’un ensemble de valeurs 32 bits. Elles s’affichent en langage HLSL (High Level Shading Language) en tant que mémoire tampon constante. Notez que les mémoires tampons constantes pour des raisons historiques sont affichées sous forme d’ensembles de valeurs 4x32 bits. <br/>                                                                                                                                        |
| [Utilisation directe des descripteurs dans la signature racine](using-descriptors-directly-in-the-root-signature.md)<br/> | Les applications peuvent placer des descripteurs directement dans la signature racine pour éviter d’avoir à passer par un tas de descripteur. Ces descripteurs occupent beaucoup d’espace dans la signature racine (voir la section limites de signature racine), de sorte que les applications doivent les utiliser avec modération. <br/>                                                                                                                                     |
| [Exemples de signatures racines](example-root-signatures.md)<br/>                                                   | La section suivante montre les signatures racines qui diffèrent en matière de complexité par rapport à la totalité de l’espace vide.<br/>                                                                                                                                                                                                                                                                                                       |
| [Spécification de signatures racines en langage HLSL](specifying-root-signatures-in-hlsl.md)<br/>                             | La spécification de signatures racines dans le modèle de nuanceur HLSL 5,1 est une alternative à leur spécification dans du code C++.<br/>                                                                                                                                                                                                                                                                                                  |
| [Signature racine version 1,1](root-signature-version-1-1.md)<br/>                                             | L’objectif de la version de signature racine 1,1 est de permettre aux applications d’indiquer aux pilotes quand les descripteurs d’un tas de descripteur ont gagné le changement ou que les descripteurs de données pointent vers le changement gagné. Cela permet aux pilotes d’effectuer des optimisations qui peuvent être possibles, sachant qu’un descripteur ou la mémoire vers laquelle il pointe est statique pendant un certain temps. <br/>                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> </dl>

 

