---
description: ICE83 valide la table MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021477"
---
# <a name="ice83"></a>ICE83

ICE83 valide la [table MsiAssembly](msiassembly-table.md). Cette action personnalisée ICE publie une erreur si le chemin d’accès de la clé pour un composant contenant un assembly Win32 est défini sur le fichier manifeste. Explicitement, l’erreur est publiée si la valeur entrée dans le champ keyPath de la [table Component](component-table.md) est égale à la valeur entrée dans le \_ champ manifeste de fichier de la table MsiAssembly. Cette action personnalisée ICE publie une erreur s’il existe au moins un enregistrement dans la table MsiAssembly et que la [table InstallExecuteSequence](installexecutesequence-table.md) ne contient pas à la fois l’action [MsiPublishAssemblies](msipublishassemblies-action.md) et l' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

## <a name="result"></a>Résultats

ICE83 publie les erreurs suivantes.



| Erreur ICE83                                                                                                   | Description                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le chemin d’accès de la clé de l’assembly SxS Win32 (composant \_ = \[ 1 \] ) ne doit pas être son fichier manifeste                       | ICE83 publie cette erreur quand le champ keyPath d’un assembly Win32 a pour valeur son fichier manifeste (composant. keyPath = = MsiAssembly. file \_ manifest). \[1 \] est le keyPath dans la table des composants                          |
| Les actions MsiPublishAssemblies et MsiUnpublishAssemblies doivent être présentes dans la table InstallExecuteSequence. | ICE83 publie cette erreur lorsqu’il existe au moins une entrée dans la table MsiAssembly, mais que la table InstallExecuteSequence ne contient pas à la fois l’action MsiAssemblyPublish et l’action MsiAssemblyUnpublish. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



