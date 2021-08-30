---
title: Utilisation de l’annotation de mappage de valeur
description: Pour obtenir un exemple de code, consultez exemple d’annotation de mappage de valeur.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e676b11cc87b4f89dec6b37438ac7176bd13d5333d40970c8f275780f3d43125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098059"
---
# <a name="using-value-map-annotation"></a>Utilisation de l’annotation de mappage de valeur

**Pour créer une carte de valeur**

1.  **Créez une chaîne de mappage.**

    Une chaîne de mappage est une liste de valeurs numériques d’un contrôle correspondant à une chaîne explicite en Unicode. Il commence par « A : » suivi d’un nombre qui indique le type d’index utilisé. Seuls les index d’images sont pris en charge ; par conséquent, le type d’index est toujours 0.

    La chaîne est suivie par les paires : index : résultat. L’index est un nombre qui représente un index d’image pour une List-View ou une vue d’arborescence, ou la valeur d’un contrôle Slider.

    La valeur obtenue est un nombre obtenu lorsque vous mappez la propriété de rôle ou d’État pour un contrôle d’affichage de liste ou d’arborescence. Ces nombres sont exprimés en décimal ou hexadécimal avec un préfixe « 0x ».

    La chaîne de mappage se termine toujours par un signe deux-points («  : ») final.

    Voici un exemple de carte d’annotation pour les propriétés d’État et de rôle d’une case à cocher dans un affichage de liste ou un contrôle d’arborescence. Il y a deux éléments dans la vue qui représentent des cases à cocher, et chacun contient des images correspondant à l’état coché et non vérifié.

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    Pour connaître les valeurs de rôle et d’état valides, consultez la section [rôles d’objet](object-roles.md) et [constantes d’état d’objet](object-state-constants.md).

    La valeur d’index peut être négative quand vous mappez des propriétés pour un contrôle Slider.

    Lorsque vous mappez une propriété de valeur ou de description, le résultat est une chaîne. Les chaînes ne sont pas placées entre guillemets et les deux-points agissent comme délimiteurs.

    Pour plus d’informations, consultez format de la [table des annotations](value-map-annotation.md).

2.  **Créez le gestionnaire d’annotations et obtenez un pointeur vers son** interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**

    Voici un exemple de création du gestionnaire d’annotations.

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  **Attachez la chaîne de mappage au contrôle.**

    Appelez [**IAccPropServices :: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), en passant le **HWND** du contrôle et un pointeur vers la chaîne de mappage.

    Le paramètre *IdProp* aura l’une des valeurs suivantes.

    

    | Paramètre                   | Usage                                                |
    |-----------------------------|---------------------------------------------------------|
    | MSAAPROPID \_ ROLEMAP         | Pour définir une carte de rôle pour les contrôles d’affichage de liste ou d’arborescence.  |
    | MSAAPROPID \_ STATEMAP        | Pour définir une table d’État pour les contrôles d’affichage de liste ou d’arborescence. |
    | \_DESCRIPTIONMAP de compte propid \_ | Pour définir une carte de description pour la vue liste ou les arborescences.   |
    | MSAAPROPID \_ VALUEMAP        | Pour définir une carte de valeur sur les contrôles Slider.                  |

    

     

4.  **Nettoyage.**

    Avant de détruire les contrôles annotés de mappage de valeur (par exemple, lors de la gestion de [WM \_ Destroy](../winmsg/wm-destroy.md)), vous devez effacer les propriétés précédemment inscrites et libérer le gestionnaire d’annotations.

    Pour ce faire, appelez [**IAccPropServices :: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) si nécessaire, puis libérez votre pointeur vers [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).

Pour obtenir un exemple de code, consultez [exemple d’annotation de mappage de valeur](value-map-annotation-sample.md).

 

 