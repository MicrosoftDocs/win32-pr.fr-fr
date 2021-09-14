---
description: Les actions personnalisées sont planifiées dans les tables de séquence de la même façon que les actions standard.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Séquencement des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7c24fb91247a36880cb808c9b8e10437312cf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230015"
---
# <a name="sequencing-custom-actions"></a>Séquencement des actions personnalisées

Les actions personnalisées sont planifiées dans les tables de séquence de la même façon que les actions standard.

**Pour planifier une action personnalisée dans une table de séquences**

1.  Entrez le nom de l’action personnalisée (qui est la clé primaire de la table [CustomAction](customaction-table.md)) dans la colonne action de la table [Sequence](sequence-table-detailed-example.md) .
2.  Entrez la séquence de l’action personnalisée relative aux autres actions du tableau dans la colonne séquence de la table de [séquences](sequence-table-detailed-example.md) . Pour plus d’informations sur les tables de séquences, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).
3.  Pour ignorer conditionnellement l’action, entrez une expression conditionnelle dans la colonne condition de la table [Sequence](sequence-table-detailed-example.md) . Le programme d’installation ignore cette action si l’expression prend la valeur FALSe.

Comme dans le cas d’actions standard, les actions personnalisées qui sont planifiées dans [InstallUISequence](installuisequence-table.md) ou [AdminUISequence](adminuisequence-table.md) s’exécutent uniquement si l’interface utilisateur interne est définie sur le niveau complet. Le niveau de l’interface utilisateur est défini à l’aide de la fonction [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

Les actions standard et personnalisées planifiées dans les tables [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) n’effectuent pas de modifications du système. Au lieu de cela, le programme d’installation met en file d’attente les enregistrements d’exécution dans un script pour une exécution ultérieure pendant le service d’installation. S’il n’existe aucun service d’installation, les actions planifiées dans ces tables sont exécutées dans le même contexte que la séquence d’interface utilisateur.

Si le serveur d’installation n’est pas inscrit, les actions personnalisées sont exécutées côté client. Si le serveur est inscrit et utilise le mode d’interface utilisateur complet, les actions personnalisées sont exécutées côté serveur.

Si vous utilisez l’interface utilisateur complète avec le serveur, les actions initiales antérieures à l’action [InstallValidate](installvalidate-action.md) sont exécutées sur le client pour permettre une interaction complète. L’exécution est ensuite basculée vers le serveur qui répète ces actions et exécute les actions d’exécution du script. Cela est suivi par un retour au client pour les actions finales.

Notez que, si un produit est supprimé en définissant sa fonctionnalité Top sur absent, la propriété [**Remove**](remove.md) ne peut pas être égale à All until après l’action [InstallValidate](installvalidate-action.md) . Cela signifie que toute action personnalisée qui dépend de REMOVE = ALL doit être séquencée après l’action InstallValidate. Une action personnalisée peut vérifier REMOVE pour déterminer si un produit a été configuré pour être complètement désinstallé.

les actions personnalisées qui font référence à un fichier installé comme source, telles que le type d’action personnalisé 17 (DLL), le type d’action personnalisé 18 (EXE), le type d’action personnalisée 21 (JScript) et le type d’action personnalisé 22 (VBScript), doivent respecter les restrictions de séquencement suivantes.

-   L’action personnalisée doit être séquencée après l’action [CostFinalize](costfinalize-action.md) afin que le chemin d’accès au fichier référencé puisse être résolu.
-   Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées différées (dans le script) doivent être séquencées après le [InstallFiles](installfiles-action.md).
-   Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées non différées doivent être séquencées après l’action [InstallInitialize](installinitialize-action.md) .

les restrictions de séquencement suivantes s’appliquent aux actions personnalisées qui modifient ou mettent à jour un package de Windows Installer.

-   Si l’action personnalisée modifie le package, par exemple en ajoutant des lignes à une table, l’action doit être séquencée avant l’action [InstallInitialize](installinitialize-action.md) .
-   Si l’action personnalisée apporte des modifications susceptibles d’affecter la rentabilité, elle doit être séquencée avant l’action [CostInitialize](costfinalize-action.md) .
-   Si l’action personnalisée modifie l’état d’installation des fonctionnalités ou des composants, elle doit être séquencée avant l’action [InstallValidate](installvalidate-action.md) .

 

 



