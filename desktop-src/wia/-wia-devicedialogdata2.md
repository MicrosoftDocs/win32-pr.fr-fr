---
description: 'Structure DEVICEDIALOGDATA2 : définit les données nécessaires pour appeler une boîte de dialogue d’appareil.'
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: DEVICEDIALOGDATA2, structure (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231089"
---
# <a name="devicedialogdata2-structure"></a>DEVICEDIALOGDATA2, structure

Définit les données nécessaires pour appeler une boîte de dialogue d’appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Spécifie la taille de cette structure en octets.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Pointe vers une interface [**IWiaItem2**](-wia-iwiaitem2.md) qui représente l’élément racine valide dans l’arborescence d’éléments de l’application.

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

**hwndParent**
</dt> <dd>

Type : **HWND**

</dd> <dd>

Spécifie le handle vers la fenêtre parente de la boîte de dialogue.

</dd> <dt>

**bstrFolderName**
</dt> <dd>

Type : **BSTR**

</dd> <dd>

Spécifie le nom du dossier dans lequel les fichiers sont transférés.

</dd> <dt>

**bstrFilename**
</dt> <dd>

Type : **BSTR**

</dd> <dd>

Spécifie le modèle de nom de fichier à utiliser pour les fichiers transférés à partir d’éléments WIA vers le dossier de destination désigné par **bstrFolderName**. Il est possible de créer un nombre arbitraire de noms de fichiers uniques en ajoutant des caractères supplémentaires au modèle de nom de fichier.

</dd> <dt>

**lNumFiles**
</dt> <dd>

Type : **long**

</dd> <dd>

Reçoit le nombre de chaînes écrites dans le tableau **pbstrFilePaths** .

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

Type : **BSTR \***

</dd> <dd>

Pointeur vers un tableau de pointeurs BSTR. Chaque élément de tableau pointe vers un BSTR qui contient le nom de destination d’un fichier qui a été transféré avec succès vers le dossier identifié par bstrFolderName. La méthode doit allouer le stockage de ce membre.

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément WIA qui transfère les données vers le ou les fichiers nommés dans le tableau **pbstrFilePaths** .

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




