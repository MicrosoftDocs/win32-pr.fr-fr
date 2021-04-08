---
title: Pages de propriétés à utiliser avec les spécificateurs d’affichage
description: Active Directory Domain Services fournir un mécanisme pour ajouter des pages à la feuille de propriétés affichée pour un objet d’annuaire à partir des composants logiciels enfichables d’administration de Active Directory ou de l’interpréteur de commandes Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- spécificateurs d’affichage AD, pages de propriétés à utiliser avec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842046"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Pages de propriétés à utiliser avec les spécificateurs d’affichage

Active Directory Domain Services fournir un mécanisme pour ajouter des pages à la feuille de propriétés affichée pour un objet d’annuaire à partir des composants logiciels enfichables d’administration de Active Directory ou de l’interpréteur de commandes Windows. Pour ajouter une page à la feuille de propriétés, implémentez une extension de feuille de propriétés.

## <a name="developer-audience"></a>Public de développeurs

Cette documentation suppose que le lecteur est familiarisé avec l’opération COM et le développement de composants à l’aide de C++. Il n’est actuellement pas possible de créer une extension de feuille de propriétés Active Directory à l’aide de Visual Basic.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Création d’une extension de feuille de propriétés Active Directory

Une *extension de feuille de propriétés* est un serveur com in-proc qui implémente certaines interfaces et est inscrit avec Active Directory Domain Services. Pour créer une extension de feuille de propriétés, procédez comme suit.

**Pour créer une extension de feuille de propriétés Active Directory**

1.  Créez la DLL d’extension de la feuille de propriétés. Une extension de feuille de propriétés est un serveur COM in-proc qui, au minimum, implémente les interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) et [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Pour plus d’informations, consultez [implémentation de l’objet com de la page de propriétés](implementing-the-property-page-com-object.md).
2.  Installez l’extension de la feuille de propriétés sur les ordinateurs où l’extension de la feuille de propriétés doit être utilisée. Pour ce faire, créez un package Microsoft Windows Installer pour la DLL d’extension de feuille de propriétés et déployez le package de manière appropriée à l’aide de la stratégie de groupe. Pour plus d’informations, consultez distribution des composants de l' [interface utilisateur](distributing-user-interface-components.md).
3.  Enregistrez l’extension de la feuille de propriétés dans le Registre Windows et avec Active Directory Domain Services. Pour plus d’informations, consultez [inscription de l’objet com de la page de propriétés dans un spécificateur d’affichage](registering-the-property-page-com-object-in-a-display-specifier.md).

 

 