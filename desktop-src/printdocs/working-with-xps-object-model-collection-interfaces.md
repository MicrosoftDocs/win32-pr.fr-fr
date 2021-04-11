---
description: Décrit comment utiliser les méthodes courantes des interfaces de collection.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Utilisation des interfaces de collection XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203468"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Utilisation des interfaces de collection XPS OM

Décrit comment utiliser les méthodes courantes des interfaces de collection.

## <a name="contents"></a>Contenu

Les méthodes décrites dans cette section s’affichent dans la liste qui suit. Toutes les interfaces de collection ne prennent pas en charge chacune de ces méthodes, et certaines interfaces prennent également en charge les méthodes qui ne sont pas décrites dans cette page. Pour obtenir la liste des méthodes prises en charge par une interface spécifique, reportez-vous à la description de la description de cette interface.

<dl>

[Append, méthode](#append-method)  
[GetAt, méthode](#getat-method)  
[GetCount, méthode](#getcount-method)  
[Méthode InsertAt](#insertat-method)  
[RemoveAt, méthode](#removeat-method)  
[Méthode SetAt](#setat-method)  
</dl>

[Voir aussi](#see-also)

## <a name="append-method"></a>Append, méthode

Ajoute un objet à la fin de la collection.

**Syntaxe générique**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**Description**

À la fin de la collection, cette méthode ajoute un objet qui est passé dans la liste de paramètres, comme indiqué dans le diagramme suivant.

![figure qui montre comment Append ajoute une entrée à la collection](images/generic-append.png)

## <a name="getat-method"></a>GetAt, méthode

Obtient un objet à partir d’un emplacement spécifié dans la collection.

**Syntaxe générique**


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



**Description**

Écrit l’objet qui est stocké à l’emplacement de la collection spécifié par *index* à la variable référencée par l' *objet*. Cette action ne modifie pas le contenu de la collection. Le diagramme suivant illustre ce processus.

![figure qui montre comment GetAt récupère une entrée de la collection](images/generic-getat.png)

## <a name="getcount-method"></a>GetCount, méthode

Obtient le nombre d’objets stockés dans la collection.

**Syntaxe générique**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**Description**

Écrit le nombre d’objets actuellement stockés dans la collection dans la variable référencée par *Count*. Cette action ne modifie pas le contenu de la collection. Le diagramme suivant illustre ce processus.

![figure qui montre comment GetCount obtient le nombre d’entrées dans la collection](images/generic-getcount.png)

## <a name="insertat-method"></a>Méthode InsertAt

Insère un objet à l’emplacement spécifié de la collection.

**Syntaxe générique**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Description**

L’objet qui est passé dans l' *objet* est inséré dans la collection à l’emplacement spécifié par l' *index*. Avant d’insérer le nouvel *objet*, cette méthode se déplace de 1 l’objet qui a occupé l’emplacement au niveau de l' *index* et déplace tous les pointeurs d’interface après l' *index*. Le diagramme suivant illustre ce processus.

![figure qui montre comment InsertAt ajoute une entrée à la collection](images/generic-insertat.png)

## <a name="removeat-method"></a>RemoveAt, méthode

Supprime l’objet à partir d’un emplacement spécifié dans la collection.

**Syntaxe générique**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Description**

Cette méthode libère l’objet à partir de l’emplacement spécifié par *index*, puis compacte la collection en réduisant de 1 l’index de chaque pointeur à la suite de l' *index*. Le diagramme suivant illustre ce processus.

![figure qui montre comment RemoveAt supprime une entrée de la collection](images/generic-removeat.png)

## <a name="setat-method"></a>Méthode SetAt

Remplace l’objet à un emplacement spécifié dans la collection.

**Syntaxe générique**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Description**

Cette méthode libère d’abord l’objet à l’emplacement référencé par l' *index*, puis remplace cet objet par celui qui est passé dans l' *objet*. Le diagramme suivant illustre ce processus.

![figure qui montre comment setat remplace une entrée dans la collection](images/generic-setat.png)

## <a name="see-also"></a>Voir aussi

<dl>

[**IXpsOMColorProfileResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[**IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[**IXpsOMFontResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[**IXpsOMGeometryFigureCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[**IXpsOMGradientStopCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[**IXpsOMImageResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[**IXpsOMSignatureBlockResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



