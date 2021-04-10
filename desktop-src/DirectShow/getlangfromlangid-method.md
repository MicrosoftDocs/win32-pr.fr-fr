---
description: La méthode GetLangFromLangID récupère une chaîne explicite lorsqu’elle reçoit un ID de langue primaire.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Méthode GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846314"
---
# <a name="getlangfromlangid-method"></a>Méthode GetLangFromLangID

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetLangFromLangID` méthode récupère une chaîne explicite lorsqu’elle reçoit un ID de langue primaire.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*
</dt> <dd>

Spécifie l’ID de langue primaire sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une représentation sous forme de chaîne de la langue qui peut être affichée dans l’interface utilisateur de l’application.

## <a name="remarks"></a>Notes

Bien que cette méthode soit nommée `GetLangFromLangID` , le paramètre que vous transmettez est en fait l’ID de langue principal, et non l’ID de langue.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



