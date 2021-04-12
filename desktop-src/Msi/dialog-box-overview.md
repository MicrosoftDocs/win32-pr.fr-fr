---
description: Le processus de création d’une boîte de dialogue dans Windows Installer est semblable au processus de création d’une boîte de dialogue par programme à l’aide d’un modèle de boîte de dialogue API Microsoft Windows.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Vue d’ensemble de la boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884c85f06bc06588084311aee370700d5b2a5290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319510"
---
# <a name="dialog-box-overview"></a>Vue d’ensemble de la boîte de dialogue

Le processus de création d’une boîte de dialogue dans Windows Installer est semblable au processus de création d’une boîte de dialogue par programme à l’aide d’un modèle de boîte de dialogue API Microsoft Windows. Lorsqu’un modèle de boîte de dialogue Windows est stocké dans une chaîne de caractères terminée par null, Windows Installer stocke les paramètres de boîte de dialogue dans la table de boîte de dialogue. La table boîte de dialogue contient une colonne attributs analogue aux styles de fenêtre dans l’API interface utilisateur Microsoft Windows. Toutefois, le nombre de bits de style de boîte de dialogue dans Windows Installer est un ensemble réduit et spécialisé.

Pour créer physiquement la boîte de dialogue à l’aide de l’API de l’interface utilisateur Windows, [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) est appelé et passe un pointeur vers le modèle. Dans Windows Installer, la boîte de dialogue est créée lors de l’exécution de l’une des trois tables de séquence d’interface utilisateur.

Windows Installer ne contient pas d’interface utilisateur par défaut que les auteurs de packages peuvent utiliser pour leurs packages. Il contient un ensemble limité de boîtes de dialogue par défaut qui affichent des messages d’erreur et d’informations, mais ceux-ci s’affichent uniquement si Windows Installer interroge les tables de la boîte de dialogue et de la séquence d’interface utilisateur et qu’aucune boîte de dialogue personnalisée n’est disponible.

Le kit de développement logiciel (SDK) d’installation inclut une base de données minimale nommée Uisample.msi qui contient des tables d’interface utilisateur et de séquence d’exécution remplies, ainsi qu’une interface utilisateur Cette base de données est facilement personnalisée et fusionnée sur n’importe quel package.

Certaines actions standard et conditions d’erreur internes Windows Installer retournent un ensemble spécifique de données d’interface utilisateur et, par conséquent, nécessitent une boîte de dialogue avec un ensemble spécifique de contrôles pour accueillir ces données. Windows Installer vérifie deux emplacements distincts pour les identificateurs de ces boîtes de dialogue.

-   Windows Installer contient un ensemble de noms de boîtes de dialogue incorporées. L’action personnalisée interroge la table de boîtes de dialogue pour ces noms réservés.
-   Dans chacune des trois tables de séquence d’interface utilisateur, les noms de boîte de dialogue avec un numéro de séquence de-1,-2 ou-3 sont affichés en réponse à la sortie, à la sortie demandée par l’utilisateur et aux messages d’erreur irrécupérables de Windows Installer.

Une liste complète des noms de boîte de dialogue de clé primaire réservée est disponible dans les [boîtes de dialogue](dialog-boxes.md). Notez que le nom de la boîte de dialogue clé primaire est réservé uniquement par le programme d’installation et qu’il n’existe aucune implémentation spécifique de la boîte de dialogue dans Windows Installer. Les auteurs de package doivent toujours remplir tous les champs de la base de données qui spécifient les attributs et les contrôles de ces boîtes de dialogue réservées.

 

 
