---
description: Une extension de composant logiciel enfichable d’une pièce jointe est le composant d’une pièce jointe qui affiche l’interface utilisateur spécifique au service.
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: Extensions du composant logiciel enfichable pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531467"
---
# <a name="attachment-snap-in-extensions"></a>Extensions du composant logiciel enfichable pièce jointe

Une extension de composant logiciel enfichable d’une pièce jointe est le composant d’une pièce jointe qui affiche l’interface utilisateur spécifique au service. L’extension du composant logiciel enfichable est hébergée par les composants logiciels enfichables de configuration de la sécurité. La communication entre l’extension de pièce jointe et son hôte de composant logiciel enfichable est gérée par les mécanismes MMC standard décrits dans la documentation de [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

En plus des interfaces que l’extension de composant logiciel enfichable doit prendre en charge pour être une extension de composant logiciel enfichable MMC, une extension de composant logiciel enfichable d’attachement doit également prendre en charge l’interface COM, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Cette interface implémente des méthodes qui indiquent s’il existe des données spécifiques au service qui doivent être enregistrées dans la base de données de sécurité et, si tel est le cas, récupérer et enregistrer ces nouvelles données. Les composants logiciels enfichables de configuration de la sécurité appellent régulièrement les méthodes de cette interface afin de mettre à jour la base de données de sécurité.

Les composants logiciels enfichables de configuration de la sécurité implémentent une interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), qui fournit des méthodes pour récupérer des données spécifiques au service à partir de la base de données de sécurité. Les extensions de composant logiciel enfichable d’attachement peuvent appeler des méthodes de cette interface pour récupérer des données de la base de données de sécurité.

Cette architecture est illustrée dans le diagramme suivant.

![extensions du composant logiciel enfichable pièce jointe](images/model2.png)

Lorsque vous créez une extension de composant logiciel enfichable d’attachement, vous devez l’installer et l’inscrire auprès des composants logiciels enfichables de configuration de sécurité. Pour ce faire, vous devez ajouter des clés au registre, comme expliqué dans [inscription d’une extension de composant logiciel enfichable d’attachement](registering-an-attachment-snap-in-extension.md). Quand un composant logiciel enfichable de configuration de sécurité démarre, il vérifie le registre et charge les extensions de composant logiciel enfichable inscrites. Les extensions apparaissent sous la forme de nœuds sous la zone sécurité pour chaque service dans le composant logiciel enfichable Configuration de la sécurité.

> [!Note]
> Une extension de composant logiciel enfichable d’une pièce jointe peut uniquement étendre des nœuds de services. Le nœud services est le composant logiciel enfichable MMC qui contient des outils pour administrer les services installés sur le système. L’extension du composant logiciel enfichable d’attachement déclare elle-même comme étant subordonnée à un type de nœud de services spécifique, puis pour chaque occurrence de ce type de nœud de services, la console MMC ajoute automatiquement les extensions de composant logiciel enfichable associées.
> 
> Chaque extension de composant logiciel enfichable en pièce jointe possède un nœud de volet d’étendue et le volet de résultats associé dans MMC.

 

 

 
