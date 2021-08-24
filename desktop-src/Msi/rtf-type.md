---
description: Le type RTF du type sémantique est l’un des types de format texte.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Type RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b378644fbf41e906993097cea8bb4fb27f969cbda046aab59700896513774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039689"
---
# <a name="rtf-type"></a>Type RTF

Le type RTF du [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md). Ce type est constitué d’une chaîne de texte arbitraire au format RTF (Rich Text Format), quelle que soit la longueur fournie par l’utilisateur. L’outil de fusion remplace cette chaîne dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « RTF » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne peut être dans n’importe quel langage compatible avec la page de codes de la base de données. consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md). NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.

 

 



