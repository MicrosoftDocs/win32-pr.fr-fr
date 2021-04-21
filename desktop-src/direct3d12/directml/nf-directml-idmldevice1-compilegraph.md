---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compile un graphique d’opérateurs DirectML dans un objet qui peut être distribué au GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803750"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>IDMLDevice1 :: CompileGraph, méthode (directml. h)

Compile un graphique d’opérateurs DirectML dans un objet qui peut être distribué au GPU.

Un opérateur compilé représente le formulaire efficace et cuit d’un opérateur apte à être exécuté sur le GPU. Un opérateur compilé conserve l’État (par exemple, les nuanceurs et autres objets) requis pour l’exécution. Comme un opérateur compilé implémente l’interface [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) , vous êtes en mesure d’en supprimer un de la mémoire du GPU si vous le souhaitez. Pour plus d’informations, consultez [IDMLDevice1 :: expulsion](/windows/win32/api/directml/nf-directml-idmldevice-evict) et [IDMLDevice1 :: MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .

L’opérateur compilé n’utilise pas ni ne référence les objets [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) fournis dans la description du graphique après le retour de cette méthode.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a>Paramètres

`desc`

Type : **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***

Description du graphique à compiler. Consultez [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Type : [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Indicateurs permettant de contrôler l’exécution de cet opérateur.

`riid`

Type : <b>REFIID</b>

Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans <i>PPV</i>. Il doit s’agir du GUID de [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).

`ppv`

Type : <b>void * *</b>

Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’opérateur compilé. Il s’agit de l’adresse d’un pointeur vers un [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), représentant l’opérateur compilé créé.


## <a name="return-value"></a>Valeur retournée

Type : [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Si cette méthode est réussie, elle retourne **S_OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes 

L’API Graph de l’opérateur DirectML fournit une méthode abstraite pour utiliser efficacement DirectML sur différents matériels. DirectML applique des optimisations de niveau tenseur, telles que le choix de la disposition de tenseur la plus efficace en fonction de l’adaptateur utilisé. Elle applique également des optimisations telles que la suppression des opérateurs de jointure ou de fractionnement.

Nous vous recommandons d’appliquer des optimisations de haut niveau avant de générer un graphique DirectML. Par exemple, le refus d’opérateurs de convolution avec BatchNorm, le repli de constante et l’élimination commune de sous-expression. Les optimisations au sein de l’optimiseur de graphique de DirectML sont destinées à compléter les optimisations indépendantes des appareils, qui sont généralement gérées de façon générique par Machine Learning frameworks.

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | directml. h |
| **Bibliothèque** | DirectML. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Voir aussi

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)