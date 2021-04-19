---
title: Méthode IWMPQuery addCondition
description: La méthode addCondition ajoute une condition à la requête composée à l’aide de et de la logique.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- méthode addCondition lecteur Windows Media
- méthode addCondition lecteur Windows Media, interface IWMPQuery
- Interface IWMPQuery lecteur Windows Media, méthode addCondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525546"
---
# <a name="iwmpqueryaddcondition-method"></a>IWMPQuery :: addCondition, méthode

La méthode **addCondition** ajoute une condition à la requête composée à l’aide **de et** de la logique.

## <a name="syntax"></a>Syntaxe


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAttribute* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’attribut à ajouter à la requête.

</dd> <dt>

*bstrOperator* \[ dans\]
</dt> <dd>

**System. String** qui est l’opérateur. Consultez la section Notes pour connaître les valeurs prises en charge.

</dd> <dt>

*bstrValue* \[ dans\]
</dt> <dd>

**System. String** qui est la valeur de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les conditions contenues dans une requête composée sont organisées en groupes de conditions. Plusieurs conditions au sein d’un groupe de conditions sont toujours concaténées à l’aide de la logique **et** . Les groupes de conditions sont toujours concaténés les uns aux autres à l’aide de **ou** logique. Pour démarrer un nouveau groupe de conditions, appelez [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).

Les requêtes composées utilisant **IWMPQuery** ne respectent pas la casse.

Une liste de valeurs pour le paramètre *bstrAttribute* se trouve dans la [référence d’attribut alphabétique](alphabetical-attribute-reference.md).

Le tableau suivant répertorie les valeurs prises en charge pour *bstrOperator*.



| String              | S’applique à     |
|---------------------|----------------|
| BeginsWith          | Chaînes        |
| Contient            | Chaînes        |
| Égal à              | Tous les types      |
| GreaterThan         | Nombres, dates |
| Supérieur ou égal à | Nombres, dates |
| LessThan            | Nombres, dates |
| Inférieur ou égal à    | Nombres, dates |
| NotBeginsWith       | Chaînes        |
| NotContains         | Chaînes        |
| NotEquals           | Tous les types      |



 

## <a name="examples"></a>Exemples

L’exemple suivant crée une requête, y ajoute deux conditions et utilise cette requête pour extraire les résultats de la requête sous la forme d’une collection de chaînes. Les résultats sont ensuite affichés dans une zone de liste. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut alphabétique**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2. createQuery (VB et C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getPlaylistByQuery (VB et C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB et C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





