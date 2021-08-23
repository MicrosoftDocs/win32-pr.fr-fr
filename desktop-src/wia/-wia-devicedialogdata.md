---
description: 'Structure DEVICEDIALOGDATA : définit les données nécessaires pour appeler une boîte de dialogue d’appareil.'
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: DEVICEDIALOGDATA, structure (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: e20b8689e71031024c46451d3079450061e8112acf1052c12129b89ed9e0a23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451199"
---
# <a name="devicedialogdata-structure"></a>DEVICEDIALOGDATA, structure

Définit les données nécessaires pour appeler une boîte de dialogue d’appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Spécifie la taille de cette structure en octets.

</dd> <dt>

**hwndParent**
</dt> <dd>

Type : **HWND**

</dd> <dd>

Spécifie le handle vers la fenêtre parente de la boîte de dialogue.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Type : **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***

</dd> <dd>

Pointe vers une interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) qui représente l’élément racine valide dans l’arborescence d’éléments de l’application.

</dd> <dt>

**dwFlags**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Spécifie un jeu d’indicateurs qui contrôlent l’opération de la boîte de dialogue. Peut être défini sur l’une des valeurs suivantes :



| Indicateur                                 | Signification                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportement par défaut                                                                                                                                                                           |
| IMAGE unique de la boîte de dialogue de l' \_ appareil WIA \_ \_ \_   | Limitez la sélection d’image à une seule image dans la boîte de dialogue acquisition d’image d’appareil.                                                                                                      |
| \_boîte de dialogue de l’appareil WIA \_ \_ utiliser \_ \_ l’interface utilisateur commune | Utilisez l’interface utilisateur du système, si elle est disponible, au lieu de l’interface utilisateur fournie par le fournisseur. Si l’interface utilisateur système n’est pas disponible, l’interface utilisateur du fournisseur est utilisée. Si aucune interface utilisateur n’est disponible, la fonction retourne E \_ NOTIMPL. |



 

</dd> <dt>

**lIntent**
</dt> <dd>

Type : **long**

</dd> <dd>

Spécifie le type de données que l’image doit représenter. Pour obtenir la liste des valeurs d’intention d’image, consultez [**constantes d’intention d’image**](-wia-imageintentconstants.md).

</dd> <dt>

**lItemCount**
</dt> <dd>

Type : **long**

</dd> <dd>

Reçoit le nombre d’éléments dans le tableau indiqué par le paramètre **ppWiaItem** .

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Type : **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Reçoit l’adresse d’un tableau de pointeurs vers des interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




