---
title: IMsTscAdvancedSettings propriété KeyBoardLayoutStr
description: Spécifie le nom de l’identificateur de paramètres régionaux d’entrée actif (anciennement appelé disposition de clavier) à utiliser pour la connexion.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété KeyBoardLayoutStr
- Services Bureau à distance de la propriété KeyBoardLayoutStr, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c87cb55b22658f704b328a51435ca2554d4c6574e25484253f9899475918642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606176"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>IMsTscAdvancedSettings :: KeyBoardLayoutStr, propriété

Spécifie le nom de l’identificateur de paramètres régionaux d’entrée actif (anciennement appelé disposition de clavier) à utiliser pour la connexion.

Si cette propriété n’est pas définie, le contrôle utilise la disposition par défaut retournée par la fonction [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom de l’identificateur de paramètres régionaux d’entrée actif.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

La propriété est un nombre hexadécimal à huit chiffres sous forme de chaîne. Les quatre chiffres inférieurs représentent l’identificateur de langue, et les quatre chiffres supérieurs représentent la variation du clavier dans cette langue. Ainsi, par exemple, « 00000409 » représente le clavier anglais américain par défaut, car « 0409 » est l’identificateur de langue Anglais (États-Unis). La variation Dvorak du clavier anglais des États-Unis a pour identificateur « 00010409 ». Vous pouvez trouver les dispositions de clavier disponibles, listées par leurs identificateurs de disposition de clavier, dans le Registre sous

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

