---
description: 'Vous avez deux possibilités lors de la compilation d’un fichier MOF : à l’aide de l’utilitaire de ligne de commande ou à l’aide d’une interface de programmation.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Exécution du compilateur MOF sur un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296607"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Exécution du compilateur MOF sur un fichier

Vous avez deux possibilités lors de la compilation d’un fichier MOF : à l’aide de l’utilitaire de ligne de commande ou à l’aide d’une interface de programmation.

Tant que vous n’avez pas exécuté le compilateur MOF, [**Mofcomp.exe**](mofcomp.md), un fournisseur n’est pas inscrit auprès de WMI et les classes qu’il a créées dans le fichier MOF ne sont pas disponibles dans l' [*espace de stockage WMI*](gloss-w.md). La procédure suivante décrit comment compiler un fichier MOF.

**Pour exécuter le compilateur MOF sur un fichier à partir de la ligne de commande**

1.  Appelez le compilateur MOF à partir de la ligne de commande, en utilisant la syntaxe suivante.

    **mofcomp** _MOFfile_**. mof**

    Le compilateur MOF prend en charge différents commutateurs pour contrôler les situations de traitement spéciales. Tous les commutateurs sont facultatifs, et toute combinaison de commutateurs est autorisée. Toutefois, il n’est pas judicieux d’utiliser certains commutateurs en combinaison avec d’autres. Par exemple, pour combiner les commutateurs **-Class : updateonly** et **-Class : CreateOnly** , le compilateur n’effectue aucune action.

    Par défaut, Mofcomp.exe stocke les classes compilées dans l' \\ espace de noms WMI par défaut racine. Notez que l’espace de noms par défaut pour Mofcomp.exe n’est pas le même que l’espace de noms par défaut pour les scripts. L’espace de noms par défaut pour les scripts est spécifié dans le contrôle WMI sous l’onglet Avancé. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).

    Vous pouvez modifier l’espace de noms qui reçoit les classes de deux manières.

    1.  Utilisez le commutateur **-N** pour la commande **mofcomp** .
    2.  Insérez l' \# [**espace de noms du pragma**](pragma-namespace.md) de commande du préprocesseur dans le fichier MOF.

2.  Si vous le souhaitez, vous pouvez compiler un fichier MOF par programme. Pour plus d’informations, consultez [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compilation des fichiers MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Commandes de préprocesseur](preprocessor-commands.md)
</dt> </dl>

 

 



