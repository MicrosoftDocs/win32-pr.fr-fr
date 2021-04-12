---
description: Étape 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Étape 4. Créer la page de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211111"
---
# <a name="step-4-create-the-property-page"></a>Étape 4. Créer la page de propriétés

À ce stade, le filtre prend en charge tout ce dont il a besoin pour une page de propriétés. L’étape suivante consiste à implémenter la page de propriétés proprement dite. Commencez par dériver une nouvelle classe de **CBasePropertyPage**. L’exemple suivant montre une partie de la déclaration, y compris certaines variables de membre privé qui seront utilisées ultérieurement dans l’exemple :


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



Ensuite, créez une ressource de boîte de dialogue dans l’éditeur de ressources, ainsi qu’une ressource de type chaîne pour le titre de la boîte de dialogue. La chaîne s’affiche dans l’onglet de la page de propriétés. Les deux ID de ressource sont des arguments du constructeur **CBasePropertyPage** :


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



L’illustration suivante montre la ressource de boîte de dialogue pour la page de propriétés exemple.

![boîte de dialogue page de propriétés](images/proppage.png)

Vous êtes maintenant prêt à implémenter la page de propriétés. Voici les méthodes de **CBasePropertyPage** à remplacer :

-   **OnConnect** est appelé lorsque le client crée la page de propriétés. Il définit le pointeur **IUnknown** sur le filtre.
-   **OnActivate** est appelé lors de la création de la boîte de dialogue.
-   **OnReceiveMessage** est appelé lorsque la boîte de dialogue reçoit un message de fenêtre.
-   **OnApplyChanges** est appelé lorsque l’utilisateur valide les modifications apportées aux propriétés en cliquant sur le bouton **OK** ou **appliquer** .
-   **OnDisconnect** est appelé lorsque l’utilisateur ignore la feuille de propriétés.

Le reste de ce didacticiel décrit chacune de ces méthodes.

Suivant : [étape 5. Stocke un pointeur vers le filtre](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



