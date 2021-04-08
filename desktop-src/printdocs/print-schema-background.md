---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Arrière-plan du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93280b6c8de62c76acdd59e2e596a0f600702451
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761564"
---
# <a name="print-schema-background"></a>Arrière-plan du schéma d’impression

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le schéma d’impression est destiné à résoudre les problèmes d’opacité et d’ambiguïté associés à la communication interne entre les composants du sous-système d’impression et à la communication externe entre le sous-système d’impression et les applications.

L’interaction actuelle du sous-système d’impression avec les plug-ins des applications et des fournisseurs de matériel utilise le binaire, la structure DEVMODE basée sur les index et le DevCaps binaire. Les paramètres définis par chaque composant sont largement opaques pour les autres composants, ce qui empêche la portabilité des paramètres entre les appareils, voire entre les différentes versions de pilote sur le même appareil. En outre, PrintCapabilities ne peut pas être facilement exploité par les applications clientes sans aucune connaissance de l’appareil ni de l’interface utilisateur du pilote. En plus de ces limitations, il n’existe pas de langage bien défini pour décrire les attributs d’appareil généraux, les PrintCapabilities, les configurations d’appareil ou la mise en forme des tâches. Le schéma d’impression et ses technologies associées sont conçus pour répondre à ces limitations, en fournissant une méthode cohérente, non ambiguë et extensible de communication des paramètres et des fonctionnalités de manière consolidée et logique.

Les bases conceptuelles des mots clés du schéma d’impression et de l’infrastructure du schéma d’impression sont cohérentes, manque d’ambiguïté et d’extensibilité. La cohérence est obtenue via l’utilisation des mots clés du schéma d’impression et de l’infrastructure du schéma d’impression comme des blocs de construction pour la communication entre les composants d’impression de nouvelle génération. Les applications, le sous-système d’impression Microsoft Windows et les plug-ins et pilotes IHV interagissent à l’aide de ce mécanisme commun. Ces mots clés, leur structure et leur signification, sont bien définis par le schéma public. Cela permet d’éviter toute ambiguïté dans le sens d’un mot clé particulier et d’éviter les mots clés redondants ou en double. Tous les composants peuvent s’appuyer sur l’utilisation d’un mot clé particulier pour indiquer une intention donnée et faire en sorte que cette intention soit bien comprise par le destinataire. L’extensibilité est essentielle pour être la longévité des mots clés du schéma d’impression, en veillant à ce que le schéma public soit une entité dynamique. La structure autorise également des extensions privées, ce qui donne aux IHV la flexibilité d’innover comme vous le souhaitez, en gardant à l’esprit que l’inclusion ultérieure d’un mot clé privé dans le schéma public est essentielle pour préserver la cohérence et empêcher toute ambiguïté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



