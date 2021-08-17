---
description: À mesure que le nombre de certificats émis dans une infrastructure à clé publique (PKI) augmente, il peut devenir difficile pour une autorité de certification unique d’effectuer un suivi efficace des certificats qu’elle a émis.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Hiérarchie des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc3420e3f0f09f88b4b9e7157ec8abacc9516520de4472a48189520e3e0e567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904973"
---
# <a name="certificate-hierarchy"></a>Hiérarchie des certificats

À mesure que le nombre de certificats émis dans une infrastructure à clé publique (PKI) augmente, il peut devenir difficile pour une autorité de certification unique d’effectuer un suivi efficace des certificats qu’elle a émis. Une façon de résoudre ce problème consiste à créer une hiérarchie de certificats dans laquelle l’autorité de certification délègue l’autorité pour émettre des certificats aux autorités subordonnées qui peuvent, à leur tour, déléguer l’autorité à leurs subordonnés. Chaque autorité de certification délègue l’autorité en émettant un certificat d’autorité de certification à un subordonné. L’autorité de certification initiale de la chaîne est appelée racine et il n’est pas nécessaire qu’une entité établisse une approbation avec une autorité de certification qui réside sur une [chaîne de certificats](about-certificate-chain.md) différente de celle sur laquelle l’entité réside.

L’illustration suivante montre une hiérarchie de certificat composée d’une autorité de certification racine, de deux autorités de certification subordonnées à la racine (une pour le service marketing et une pour le service de fabrication) et d’autorités de certification subordonnées à celles-ci.

![diagramme de la hiérarchie des certificats](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles d’approbation](about-trust-models.md)
</dt> </dl>

 

 



