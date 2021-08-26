---
description: Définition des propriétés des effets et des transitions
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Définition des propriétés des effets et des transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1305eb7860b5519b14cfeebc349643c2662db3f133c0bf3424d1d71ccf85753c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904259"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Définition des propriétés des effets et des transitions

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

de nombreux DirectShow des effets et des transitions de [Services d’édition](directshow-editing-services.md) prennent en charge des propriétés qui contrôlent leur comportement. Une application peut définir la valeur d’une propriété à l’aide de l’interface [**IPropertySetter**](ipropertysetter.md) . L’effet sous-jacent ou l’objet de transition doit prendre en charge **IDispatch** pour définir les propriétés. Avec les effets vidéo et les transitions, l’application peut définir une plage de valeurs qui changent au fil du temps. (Par exemple, vous pouvez définir une transition de réinitialisation pour vous déplacer d’une image à l’autre.) Avec les effets audio, la valeur de la propriété est statique et ne peut pas changer au fil du temps. La seule exception est l’effet d' [enveloppe de volume](volume-envelope-effect.md) , qui prend en charge une propriété dynamique pour le niveau de volume.

Pour définir une propriété, procédez comme suit.

1.  Créez une instance de l’accesseur Set de propriété (CLSID \_ PropertySetter).
2.  Remplissez les structures de [**\_ valeur**](dexter-value.md) [**Dexter \_**](dexter-param.md) et Dexter avec les données de propriété. Ces structures sont décrites ci-dessous.
3.  Transmettez les structures de [**\_ valeur**](dexter-value.md) [**Dexter \_**](dexter-param.md) et Dexter à la méthode [**IPropertySetter :: AddProp**](ipropertysetter-addprop.md) .
4.  Répétez les étapes 2 et 3 pour chaque propriété que vous souhaitez définir.
5.  Transmettez le pointeur d’interface [**IPropertySetter**](ipropertysetter.md) à la méthode [**IAMTimelineObj :: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .

La structure de [**\_ paramètre Dexter**](dexter-param.md) spécifie la propriété qui est définie. Il contient les membres suivants.

-   **Nom**: nom de la propriété
-   **DISPID**: réservé, doit être égal à zéro
-   **nvaleurs**: nombre de valeurs

La \_ structure de valeur Dexterity spécifie la valeur d’une propriété à un moment donné. Il contient les membres suivants.

-   **v**: type Variant qui spécifie une nouvelle valeur pour la propriété. Le membre **VT** de cette variante définit le type de données de la propriété. pour plus d’informations sur le type **VARIANT** , consultez le SDK Windows.
-   **RT**: temps de référence lorsque la propriété suppose cette valeur, par rapport à l’heure de début de l’effet ou de la transition. L’heure de début de l’effet ou de la transition est relative à l’heure de début de son objet parent.
-   **dwInterp**: indicateur qui spécifie la façon dont la propriété passe de la valeur précédente à la nouvelle valeur. Avec l' \_ indicateur de saut DEXTERF, la propriété passe instantanément à la nouvelle valeur à l’heure spécifiée. Avec l' \_ indicateur d’interpolation DEXTERF, la propriété est interpolée de façon linéaire par rapport à la valeur précédente.

Si vous définissez le membre **VT** sur VT \_ BSTR, la méthode setter de la propriété effectue toutes les conversions nécessaires. Pour les valeurs à virgule flottante, incluez le zéro non significatif avant la décimale. Par exemple, 0,3, pas. 3.

> [!Note]  
> Les applications doivent éviter de se reposer sur la conversion de **BSTR** en valeurs numériques. Si la propriété a une valeur numérique, utilisez le type de **variante** numérique approprié est possible.

 

La valeur d’une propriété pouvant changer au fil du temps, la méthode [**IPropertySetter :: AddProp**](ipropertysetter-addprop.md) prend une structure de [**\_ paramètre Dexter**](dexter-param.md) unique et un pointeur vers un tableau de structures de [**\_ valeur Dexterity**](dexter-value.md) . Le tableau définit un ensemble de valeurs basées sur le temps pour la propriété. Les membres du tableau doivent être dans l’ordre chronologique croissant et le membre **nvaleurs** de la \_ structure de paramètre Dexter doit être égal à la longueur du tableau.

L’exemple de code suivant crée des données de propriété pour la transition de [réinitialisation SMPTE](smpte-wipe-transition.md) . Elle définit le code de réinitialisation sur 120, ce qui crée une effacement ovale. Elle définit le temps de référence à zéro, ce qui indique le début de la transition.


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



**Modification dynamique des propriétés**

Une fois que vous avez rendu un projet de montage vidéo, il est possible de modifier les propriétés d’un objet d’effet ou de transition pendant que le graphique est en cours d’exécution. Toutefois, cela n’est possible que si vous définissez des propriétés sur cet objet avant l’application appelée [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md). Dans ce cas, vous pouvez appeler [**IAMTimelineObj :: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) sur l’effet ou la transition, effacer ou modifier les propriétés, et les modifications se produisent de manière dynamique à mesure que le graphique est en cours d’exécution. Il peut y avoir des anomalies visuelles pendant que la modification se produit, ce qui est recommandé uniquement pour la version préliminaire. Ne modifiez pas les propriétés lorsque vous écrivez le projet dans un fichier.

Si vous n’avez pas défini de propriétés sur l’objet d’effet ou de transition avant d’appeler **ConnectFrontEnd**, vous ne pouvez pas lui ajouter de propriétés pendant que le graphique est en cours d’exécution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



