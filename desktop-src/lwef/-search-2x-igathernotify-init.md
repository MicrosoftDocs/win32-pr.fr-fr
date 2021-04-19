---
title: IGatherNotify init (déconseillé), méthode
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | IGatherNotify init (déconseillé), méthode
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Méthode Init (déconseillée) fonctionnalités héritées de l’environnement Windows
- Méthode Init (obsolète) fonctionnalités héritées de l’environnement Windows, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode Init (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538046"
---
# <a name="igathernotifyinit-deprecated-method"></a>IGatherNotify :: init (déconseillé), méthode

\[**Init** peut être modifié ou non disponible dans les versions ultérieures du système d’exploitation ou du produit.\]

Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.

Initialise l’interface du Rassembleur. Spécifie également l’index à notifier et le magasin d’applications à surveiller.

## <a name="syntax"></a>Syntaxe


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrApplication* \[ dans\]
</dt> <dd>

Type : **BSTR**

Chaîne qui spécifie l’application cible.

</dd> <dt>

*bstrProject* \[ dans\]
</dt> <dd>

Type : **BSTR**

Chaîne qui spécifie le nom de l’indexeur auquel transmettre les informations du Rassembleur.

</dd> <dt>

*varScopesBstrArray* \[ dans\]
</dt> <dd>

Type : **variante**

Paramètre facultatif qui vous permet de passer un tableau d’étendues à initialiser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Initialize with application = "RSApp", Project = "MyIndex".

 

 
