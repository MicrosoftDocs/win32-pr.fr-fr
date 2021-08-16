---
description: La classe CBasePropertyPage est une classe abstraite pour l’implémentation d’une page de propriétés. Utilisez cette classe si vous écrivez un filtre (ou un autre objet) qui prend en charge les pages de propriétés.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: CBasePropertyPage, classe (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ca4bf0789488a8601ae24bd4e43e1af8335fdf97a7864cbfba242b9c99eca8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955012"
---
# <a name="cbasepropertypage-class"></a>CBasePropertyPage, classe

![hiérarchie de la classe CBasePropertyPage](images/cprop01.png)

La `CBasePropertyPage` classe est une classe abstraite pour l’implémentation d’une page de propriétés. Utilisez cette classe si vous écrivez un filtre (ou un autre objet) qui prend en charge les pages de propriétés.



| Variables membres protégées                                             | Description                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bDirty**](cbasepropertypage-m-bdirty.md)                        | Indique si l’une des propriétés a changé.                                                                             |
| [**m \_ DialogId**](cbasepropertypage-m-dialogid.md)                    | Identificateur de ressource pour la boîte de dialogue.                                                                                               |
| [**m \_ DLG**](cbasepropertypage-m-dlg.md)                              | Handle de la fenêtre de boîte de dialogue.                                                                                                      |
| [**HWND de m \_**](cbasepropertypage-m-hwnd.md)                            | Handle de la fenêtre de boîte de dialogue.                                                                                                      |
| [**m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)                  | Pointeur vers l’interface **IPropertyPageSite** du site de la page de propriétés.                                                         |
| [**m \_ TitleId**](cbasepropertypage-m-titleid.md)                      | Identificateur de ressource pour une chaîne qui contient le titre de la boîte de dialogue.                                                                  |
| M&#233;thodes publiques                                                         | Description                                                                                                                       |
| [**CBasePropertyPage**](cbasepropertypage-cbasepropertypage.md)       | Méthode de constructeur.                                                                                                               |
| [**~ CBasePropertyPage**](cbasepropertypage--cbasepropertypage.md)     | Méthode de destructeur. Virtuels.                                                                                                       |
| [**Activé**](cbasepropertypage-onactivate.md)                     | Appelé lorsque la page de propriétés est activée. Virtuels.                                                                              |
| [**OnApplyChanges**](cbasepropertypage-onapplychanges.md)             | Appelé lorsque l’utilisateur applique des modifications à la page de propriétés. Virtuels.                                                               |
| [**OnConnect**](cbasepropertypage-onconnect.md)                       | Fournit un pointeur **IUnknown** vers l’objet associé à la page de propriétés. Virtuels.                                        |
| [**Désactivé**](cbasepropertypage-ondeactivate.md)                 | Appelé lorsque la fenêtre de boîte de dialogue est détruite. Virtuels.                                                                          |
| [**OnDisconnect**](cbasepropertypage-ondisconnect.md)                 | Appelé lorsque la page de propriétés doit libérer l’objet associé. Virtuels.                                                      |
| [**OnReceiveMessage**](cbasepropertypage-onreceivemessage.md)         | Appelé lorsque la boîte de dialogue reçoit un message. Virtuels.                                                                           |
| Méthodes IPropertyPage                                                  | Description                                                                                                                       |
| [**Activer**](cbasepropertypage-activate.md)                         | Crée la fenêtre de boîte de dialogue.                                                                                                    |
| [**Appliquer**](cbasepropertypage-apply.md)                               | Applique les valeurs de page de propriétés actuelles à l’objet associé à la page de propriétés.                                          |
| [**Désactivation**](cbasepropertypage-deactivate.md)                     | Détruit la fenêtre de boîte de dialogue.                                                                                                       |
| [**GetPageInfo**](cbasepropertypage-getpageinfo.md)                   | Récupère des informations sur la page de propriétés.                                                                                    |
| [**Aide**](cbasepropertypage-help.md)                                 | Appelle l’aide de la page de propriétés.                                                                                                   |
| [**IsPageDirty**](cbasepropertypage-ispagedirty.md)                   | Indique si la page de propriétés a été modifiée depuis son activation ou depuis l’appel le plus récent à **IPropertyPage :: apply**. |
| [**Activer**](cbasepropertypage-move.md)                                 | Positionne et redimensionne la boîte de dialogue.                                                                                             |
| [**SetObjects**](cbasepropertypage-setobjects.md)                     | Fournit des pointeurs **IUnknown** pour les objets associés à la page de propriétés.                                                 |
| [**SetPageSite**](cbasepropertypage-setpagesite.md)                   | Initialise la page de propriétés.                                                                                                    |
| [**Afficher**](cbasepropertypage-show.md)                                 | Affiche ou masque la boîte de dialogue.                                                                                                    |
| [**TranslateAccelerator**](cbasepropertypage-translateaccelerator.md) | Indique à la page de propriétés de traiter une séquence de touches.                                                                               |



 

## <a name="remarks"></a>Remarques

Une page de propriétés étant un objet COM, vous devez générer un GUID pour l’identificateur de classe (CLSID) et fournir une entrée dans le tableau [**CFactoryTemplate**](cfactorytemplate.md) . pour plus d’informations, consultez [DirectShow et COM](directshow-and-com.md). L’exemple suivant illustre une entrée de fabrique de classes typique :


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



Votre filtre doit exposer l’interface **ISpecifyPropertyPages** . Cette interface contient une méthode unique, **GetPages**, qui retourne le CLSID de la page de propriétés. L’exemple suivant montre comment implémenter cette méthode :


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



N’oubliez pas de remplacer la méthode **NonDelegatingQueryInterface** du filtre. pour plus d’informations, consultez [DirectShow et COM](directshow-and-com.md) et [**INonDelegatingUnknown**](inondelegatingunknown.md).

Ensuite, créez la boîte de dialogue en tant que ressource dans votre projet, puis créez une ressource de type chaîne qui contient le titre de la boîte de dialogue. Ces deux ID de ressource sont des paramètres du constructeur **CBasePropertyPage** . Si vous conservez la chaîne de titre dans une ressource, il est plus facile de localiser la page de propriétés.

La classe **CBasePropertyPage** fournit une infrastructure pour l’interface **IPropertyPage** . Ce Framework appelle plusieurs méthodes virtuelles, notamment [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md), etc. Dans la classe de base, ces méthodes retournent simplement S \_ OK. Votre classe dérivée doit substituer une partie ou l’ensemble de ces méthodes virtuelles. Pour plus d’informations, consultez les notes relatives aux différentes méthodes.

Pour obtenir un exemple étendu de l’utilisation de cette classe pour créer une page de propriétés, consultez [création d’une page de propriétés de filtre](creating-a-filter-property-page.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




