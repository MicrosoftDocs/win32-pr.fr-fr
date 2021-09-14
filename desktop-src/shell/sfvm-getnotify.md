---
description: Notification envoyée à l’objet de rappel d’affichage pour spécifier les emplacements et les événements qui doivent être enregistrés pour les événements de notification de modification.
title: Message SFVM_GETNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235152"
---
# <a name="sfvm_getnotify-message"></a>\_Message SFVM GETNOTIFY

Notification envoyée à l’objet de rappel d’affichage pour spécifier les emplacements et les événements qui doivent être enregistrés pour les événements de notification de modification. Une fois qu’ils sont inscrits, quand une modification se produit dans sur ces emplacements ou événements, l’objet de rappel de vue est notifié. Ces événements sont envoyés au rappel de la vue via [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) et sont ensuite gérés par la vue.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PIDL* \[ à\]
</dt> <dd>

Pointeur vers un IDList absolu d’un élément pour lequel la vue doit s’inscrire pour être avertie des modifications. En règle générale, il s’agit du même IDList que l’emplacement affiché, mais il peut s’agir d’un autre emplacement.

> [!IMPORTANT]
> La durée de vie de cette valeur est la propriété de l’objet de rappel de la vue. Il est de la responsabilité de l’objet de rappel de vue de créer, puis de libérer cette valeur lorsqu’il n’est plus nécessaire. Cela nécessite que l’objet de rappel de vue stocke cette valeur. En règle générale, la valeur peut être stockée dans le membre **\_ pidlMonitor** de l’objet de rappel de la vue. Les règles de propriété pour la valeur retournée via *PIDL* sont non standard et nécessitent une attention particulière. L’objet de rappel de vue doit posséder cette valeur et s’assurer qu’il n’est pas libéré tant que l’objet de rappel d’affichage lui-même n’est pas détruit.

 

</dd> <dt>

*lEvents* \[ à\]
</dt> <dd>

Valeur qui contient une ou plusieurs valeurs SHCNE. Pour obtenir la liste des valeurs possibles, consultez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) . L’objet de rappel d’affichage s’inscrit pour recevoir un message [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) lorsque l’un des événements associés se produit.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ignoré, mais doit retourner S \_ OK.

## <a name="remarks"></a>Notes

Si ce message de rappel ne retourne pas une valeur différente de zéro pour le IDList ou le masque d’événements, la vue n’est pas inscrite pour les notifications de modification.

## <a name="examples"></a>Exemples

L’exemple suivant montre un exemple d’implémentation du code du gestionnaire de la fonction de rappel d’affichage pour **SFVM \_ GETNOTIFY**.


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SFVM \_ QUERYFSNOTIFY**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
