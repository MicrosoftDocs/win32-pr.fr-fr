---
description: La fonction d’exportation FormatProperties met en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau. Si vous souhaitez afficher des données dans le volet d’informations, vous devez implémenter la fonction d’exportation FormatProperties dans toutes les dll de l’analyseur.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Fonction de rappel FormatProperties (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544212"
---
# <a name="formatproperties-callback-function"></a>FormatProperties fonction de rappel

La fonction d’exportation **FormatProperties** met en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau. Si vous souhaitez afficher des données dans le volet d’informations, vous devez implémenter la fonction d’exportation **FormatProperties** dans toutes les dll de l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame en cours d’analyse.

</dd> <dt>

*lpFrame* \[ dans\]
</dt> <dd>

Pointeur vers le premier octet d’un frame.

</dd> <dt>

*lpProtocol* \[ dans\]
</dt> <dd>

Pointeur vers le début des données de protocole dans un frame.

</dd> <dt>

*nPropertyInsts* \[ dans\]
</dt> <dd>

Nombre de structures [PROPERTYINST](propertyinst.md) fournies par *lpPropInst*.

</dd> <dt>

*lpPropInst* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de structures [PROPERTYINST](propertyinst.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Moniteur réseau appelle la fonction **FormatProperties** pour afficher les données dans le volet d’informations de l’interface utilisateur Moniteur réseau. En règle générale, **FormatProperties** est appelé pour mettre en forme la ligne de résumé pour un protocole, puis pour mettre en forme toutes les instances de propriété du protocole dans un frame. Toutefois, Moniteur réseau ne garantit pas le nombre de fois où il appelle **FormatProperties** pour un analyseur spécifique.

Pendant l’implémentation de la fonction **FormatProperties** , l’analyseur appelle indirectement la fonction [FormatPropertyInstance](formatpropertyinstance.md) pour utiliser le formateur générique fourni par Moniteur réseau, ou il peut appeler une procédure de formateur personnalisée définie par l’analyseur. L’un des formateurs doit être appelé pour chaque structure [PROPERTYINST](propertyinst.md) transmise à la dll de l’analyseur dans le paramètre *lpPropInst* .



| Pour plus d’informations sur                                          | Consultez                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.   | [Analyseurs](parsers.md)                                             |
| Les points d’entrée inclus dans la DLL de l’analyseur.          | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)             |
| L’implémentation de **FormatProperties**  comprend un exemple. | [Implémentation de FormatProperties](implementing-formatproperties.md) |
| Comment le formateur générique formate les différents types de données.  | [Sortie de formateur générique](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




