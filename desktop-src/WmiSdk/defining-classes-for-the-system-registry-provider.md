---
description: Une application de gestion utilisant le fournisseur de Registre système peut définir des classes avec des propriétés qui représentent des données de Registre pour des clés particulières, puis stocke les classes dans le référentiel WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Définition des classes pour le fournisseur de Registre système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952550"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Définition des classes pour le fournisseur de Registre système

Une application de gestion utilisant le fournisseur de Registre système peut définir des classes avec des propriétés qui représentent des données de Registre pour des clés particulières, puis stocke les classes dans le référentiel WMI. La plupart des processus de définition d’une classe pour le registre système sont identiques à la définition d’une autre classe. Toutefois, le fournisseur de Registre système nécessite que vous utilisiez des qualificateurs et des types de données spécifiques.

La procédure suivante décrit comment définir une classe pour le fournisseur de Registre système.

**Pour définir une classe pour le fournisseur de Registre système**

1.  Créez la classe comme vous le feriez pour toute autre classe.

    Pour plus d’informations, consultez [création d’une classe](creating-a-class.md).

2.  Mappez les types de données de registre appropriés aux types WMI appropriés.

    Le fournisseur de Registre système mappe les types de données de Registre à des types de données WMI spécifiques. Pour plus d’informations, consultez [mappage d’un type de données de Registre à un type de données WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Utilisez les qualificateurs requis pour définir l’emplacement du fournisseur du Registre et l’emplacement de la clé de registre appropriée.

    Le fournisseur de Registre système utilise trois qualificateurs pour définir l’emplacement de diverses classes, fournisseurs et entrées de registre. Pour plus d’informations, consultez [définition d’une classe de Registre avec des qualificateurs](defining-a-registry-class-with-qualifiers.md).

 

 



