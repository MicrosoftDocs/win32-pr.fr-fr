---
title: Instructions de programmation Services Bureau à distance
description: Rubriques qui fournissent des instructions pour le développement d’applications dans un environnement de Services Bureau à distance.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, instructions de programmation
- instructions de programmation Services Bureau à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106536889"
---
# <a name="remote-desktop-services-programming-guidelines"></a>Instructions de programmation Services Bureau à distance

La plupart des applications Windows 32 bits ou 64 bits existantes s’exécutent « en l’environnement » dans une Services Bureau à distance (anciennement « services Terminal Server »). Toutefois, certaines applications fonctionnent correctement et fonctionnent bien dans un environnement Services Bureau à distance, contrairement à d’autres. Les rubriques suivantes fournissent des instructions pour le développement d’applications dans un environnement de Services Bureau à distance.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Instructions pour plusieurs utilisateurs](multiple-user-guidelines.md)
</dt> <dd>

Instructions pour le développement d’applications pour plusieurs utilisateurs dans un environnement de Services Bureau à distance.

</dd> <dt>

[Instructions relatives aux performances](performance-guidelines.md)
</dt> <dd>

Instructions pour le développement d’applications qui fonctionnent correctement dans un environnement de Services Bureau à distance.

</dd> <dt>

[Instructions de programmation générales](general-programming-guidelines.md)
</dt> <dd>

Instructions pour le développement d’applications dans un environnement de Services Bureau à distance.

</dd> </dl>

La plupart de ces instructions sont de bonnes pratiques en matière de programmation qui tireront parti des applications qui s’exécutent dans n’importe quel environnement Windows. Toutefois, certaines optimisations recommandées, telles que la limitation des effets graphiques, sont des optimisations que vous souhaiteriez uniquement lorsque votre application s’exécute sous Services Bureau à distance. Pour obtenir un exemple de code qui montre comment détecter un environnement de Services Bureau à distance, consultez [détection de l’environnement services Bureau à distance](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>


</dt> <dt>

[Les services Terminal Server sont désormais Services Bureau à distance](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Format du fichier de modèle d’administration](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[Sécurité de la clé de Registre et droits d’accès](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[Ruches du Registre](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[Descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[Droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modèle de Access Control](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 