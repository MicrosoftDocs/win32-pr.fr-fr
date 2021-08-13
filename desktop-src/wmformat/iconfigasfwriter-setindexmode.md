---
title: Méthode IConfigAsfWriter SetIndexMode
description: La méthode SetIndexMode permet à l’application de contrôler si le fichier sera indexé temporellement.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Méthode SetIndexMode format Windows Media
- Méthode SetIndexMode format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b65fbd3d279b8a66c132d24476b09b0f897c5993ea9a97d86096cf856832f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433609"
---
# <a name="iconfigasfwritersetindexmode-method"></a>IConfigAsfWriter :: SetIndexMode, méthode

La méthode **SetIndexMode** permet à l’application de contrôler si le fichier sera indexé temporellement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bIndexFile* \[ dans\]
</dt> <dd>

Variable de type **bool**; **True** spécifie que le fichier sera indexé temporellement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Par défaut, l' [enregistreur ASF WM](wm-asf-writer-filter.md) crée des fichiers ASF indexés de façon temporelle. Il effectue l’indexation lorsque le graphique s’arrête. Vous pouvez désactiver ce comportement si vous souhaitez effectuer votre propre indexation basée sur des trames en tant qu’étape de traitement. pour créer un fichier d’index de frames, appelez **SetIndexMode**(false), créez le fichier, puis utilisez les méthodes Windows du kit de développement logiciel (SDK) de Format de média directement pour créer un index basé sur des frames pour le fichier.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 