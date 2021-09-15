---
description: que vous choisissiez de convertir vos packages MTS en applications COM+ manuellement ou que le processus d’installation de Microsoft Windows le fasse automatiquement, vous devez être conscient des résultats de la conversion, ainsi que des problèmes rencontrés.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Résultats et problèmes de conversion COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403552"
---
# <a name="com-conversion-results-and-issues"></a>Résultats et problèmes de conversion COM+

que vous choisissiez de convertir vos packages MTS en applications COM+ manuellement ou que le processus d’installation de Microsoft Windows le fasse automatiquement, vous devez être conscient des résultats de la conversion, ainsi que des problèmes rencontrés.

## <a name="what-is-converted"></a>Ce qui est converti

Au cours de la conversion, l’utilitaire MTSTOCOM convertit les rôles, les attributions de rôles, les interfaces, les méthodes, les utilisateurs, la liste des ordinateurs et la plupart des paramètres de l’ordinateur. L’utilitaire MTSTOCOM convertit également l’identité et le mot de passe d’un package MTS.

Les nouveaux attributs COM+ qui n’étaient pas disponibles dans MTS sont automatiquement définis sur les valeurs par défaut suivantes pour tous les composants MTS convertis. Ces valeurs par défaut peuvent être modifiées à l’aide de l’outil d’administration Services de composants ou des interfaces d’administration COM+.

-   Activation JIT activée.
-   Mise en pool d’objets désactivée.
-   Synchronisation identique au paramètre de transaction.

## <a name="conversion-issues"></a>Problèmes de conversion

COM+ est installé automatiquement lorsque vous installez Windows. Il n’est pas possible de désinstaller COM+. Les problèmes liés aux mises à niveau des installations MTS et COM+ existantes sont les suivants :

-   Si vous utilisez actuellement MTS 1,0, MTS est automatiquement mis à niveau vers COM+. Toutefois, les packages définis par l’utilisateur sont perdus et vous devez les recréer.
-   Si vous utilisez actuellement MTS 2,0, MTS est automatiquement mis à niveau vers COM+. Tous les packages définis par l’utilisateur seront mis à niveau vers les applications COM+. Tous les composants doivent fonctionner comme dans MTS 2,0.
-   Si vous utilisez MTS 1,0 et MTS 2,0 et que vous avez installé l’option du kit de développement logiciel (SDK), les fichiers du SDK seront supprimés. vous pouvez installer la dernière version du kit de développement logiciel (SDK) COM+ via le Microsoft Windows SDK.
-   Vous ne pouvez pas gérer un ordinateur MTS distant à partir d’un ordinateur COM+.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion automatique à partir de MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Conversion manuelle à partir de MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Bibliothèque d’administration MTS](mts-administration-library.md)
</dt> </dl>

 

 



