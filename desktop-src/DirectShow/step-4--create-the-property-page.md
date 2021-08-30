---
description: implémentez une page de propriétés dans le cadre de la création d’une page de propriétés de filtre pour un filtre de DirectShow personnalisé.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Étape 4. Créer la page de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cfc2847757e84eb7c59984a6f5042339d2d796562b92cbf7581a9ffb12b012
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107603"
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

 

 



