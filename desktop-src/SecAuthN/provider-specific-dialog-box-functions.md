---
description: Les fonctions de boîte de dialogue spécifiques au fournisseur permettent à un fournisseur d’afficher et de gérer des informations spécifiques au réseau en modifiant des boîtes de dialogue système ou en affichant des boîtes de dialogue personnalisées.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific les fonctions de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d31a38f09dd0e0806fe21f491d02b5e18fe0abb1e5a181e40f0ab6370280b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920576"
---
# <a name="provider-specific-dialog-box-functions"></a>Provider-Specific les fonctions de boîte de dialogue

Les fonctions de boîte de dialogue spécifiques au fournisseur permettent à un fournisseur d’afficher et de gérer des informations spécifiques au réseau en modifiant des boîtes de dialogue système ou en affichant des boîtes de dialogue personnalisées.

Les fonctions de boîte de dialogue suivantes ajoutent des boutons à la boîte de dialogue **Propriétés** du gestionnaire de fichiers. Le fournisseur peut ensuite gérer les événements de ces boutons pour effectuer des tâches spécifiques au réseau. Notez qu’il existe une limite au nombre de boutons qui peuvent être ajoutés. Pour cette raison, les fournisseurs doivent utiliser cette fonctionnalité avec modération. En outre, un fournisseur peut ne pas être en mesure d’ajouter un bouton, car l’espace disponible a déjà été utilisé par d’autres fournisseurs. Un fournisseur de réseau doit gérer cette situation.



| Fonction                                           | Description                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Détermine les noms des boutons ajoutés à une boîte de dialogue de propriétés pour une ressource spécifique.<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Appelée lorsqu’un utilisateur clique sur un bouton ajouté à l’aide de la fonction [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Permet aux fournisseurs réseau d’implémenter leur propre fonctionnalité de recherche au-delà de celle fournie dans la boîte de dialogue de **connexion** .<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Permet aux fournisseurs de réseau de mettre en forme ou de modifier des noms réseau avant qu’ils ne soient présentés à l’utilisateur.<br/>                 |



 

 

 




