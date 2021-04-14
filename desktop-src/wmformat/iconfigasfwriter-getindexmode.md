---
title: Méthode IConfigAsfWriter GetIndexMode
description: La méthode GetIndexMode récupère le mode d’index temporel actuel.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Méthode GetIndexMode format Windows Media
- Méthode GetIndexMode format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382211"
---
# <a name="iconfigasfwritergetindexmode-method"></a>IConfigAsfWriter :: GetIndexMode, méthode

La méthode **GetIndexMode** récupère le mode d’index temporel actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbIndexFile* \[ à\]
</dt> <dd>

Pointeur vers une variable de type **bool** qui reçoit le paramètre de mode d’index temporel. La valeur **true** indique que l’enregistreur ASF WM est configuré pour écrire des fichiers indexés temporellement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Utilisez cette méthode pour déterminer si l' [enregistreur ASF WM](wm-asf-writer-filter.md) est actuellement configuré pour écrire des fichiers ASF indexés temporellement. Pour plus d’informations sur les fichiers indexés et indexés dans le cadre d’une indexation temporelle, consultez les notes pour [**IConfigAsfWriter :: SetIndexMode**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 