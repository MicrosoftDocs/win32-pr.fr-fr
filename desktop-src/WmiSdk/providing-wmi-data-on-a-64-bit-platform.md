---
description: Les scripts et les applications écrits pour les systèmes d’exploitation 32 bits doivent continuer à fonctionner correctement.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Fourniture de données WMI sur une plateforme 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cb8a7e698723c6d4705a735591097fe7cf354db9684924d58f6b363c0ae6b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992639"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>Fourniture de données WMI sur une plateforme 64 bits

Les scripts et les applications écrits pour les systèmes d’exploitation 32 bits doivent continuer à fonctionner correctement. Si vous disposez déjà d’un fournisseur 32 bits, vous pouvez évaluer si vous devez écrire une version 64 bits pour une opération côte à côte. En règle générale, les deux versions ne sont pas nécessaires et la version 64 bits peut traiter à la fois les clients locaux et distants 32 bits et 64 bits. Toutefois, pour le mode de compatibilité des applications 32 bits, utilisez votre fournisseur WMI 32 bits existant sur un système 64 bits qui s’exécute en mode WOW64 32 bits.

Dans de rares cas, les fournisseurs 32 bits et 64 bits doivent s’exécuter côte à côte sur des systèmes 64 bits. Dans ce cas, la version appropriée du fournisseur qui est chargée varie selon que l’appelant est 32-bit ou 64 bits et local ou distant. Un appelant qui utilise les indicateurs de contexte de l’objet de connexion, **\_ \_ ProviderArchitecture** et **\_ \_ RequiredArchitecture**, peut demander à ce que WMI charge un fournisseur non défini par défaut. Pour plus d’informations, consultez [obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).

Dans le cas rare où vous devez exécuter les fournisseurs 32 bits et 64 bits côte à côte, vous devez vous assurer que les scénarios d’installation et de désinstallation sont gérés avec précaution. Cela est dû au fait que WMI n’a qu’un seul [*référentiel*](gloss-w.md) et que les versions 32 bits et 64 bits de [**mofcomp.exe**](mofcomp.md) placent les données dans le même référentiel ; Il n’existe aucune distinction entre un fichier. mof 32 bits ou 64. La réinstallation d’une version du fournisseur n’a pas d’impact : les fichiers. mof seront compilés et les classes stockées dans le référentiel. Toutefois, une deuxième désinstallation qui supprime un espace de noms peut interférer avec le fonctionnement de l’autre fournisseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[Demande de données WMI sur une plateforme 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fourniture de données à WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



