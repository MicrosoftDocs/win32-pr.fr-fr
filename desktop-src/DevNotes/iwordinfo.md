---
description: L’interface IWordInfo est un composant de ressource de langue spécifique au japonais. L’objet analyse le texte et identifie les mots individuels, en retournant les mots de la chaîne ou retourne les formes de dictionnaire (racine) des mots dans le texte de la chaîne.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interface IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: a82ff0c5d817dbec6d64d1d38d40245983877563416b30760926bb7522cd14c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001469"
---
# <a name="iwordinfo-interface"></a>Interface IWordInfo

\[cette interface est obsolète et n’est pas prise en charge sur Windows Vista.\]

L’interface **IWordInfo** est un composant de ressource de langue spécifique au japonais. L’objet analyse le texte et identifie les mots individuels, en retournant les mots de la chaîne ou retourne les formes de dictionnaire (racine) des mots dans le texte de la chaîne.

## <a name="members"></a>Membres

L’interface **IWordInfo** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWordInfo** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWordInfo** possède ces méthodes.



| Méthode        | Description                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | Analyse le texte pour identifier les mots et fournit les résultats à l’objet [WordSink](/previous-versions//ms691570(v=vs.85)) .<br/> |



 

## <a name="remarks"></a>Remarques

Cette interface est utilisée pour récupérer les césures lexicales ou les formulaires de dictionnaire du texte à analyser. Le format de dictionnaire d’un mot est le formulaire uninflected du mot.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                  |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
