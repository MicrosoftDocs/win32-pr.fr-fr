---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Génère une liste d’objets adaptateur représentant l’état actuel de l’adaptateur du système et répondant aux critères spécifiés.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463459"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>IDXCoreAdapterFactory :: CreateAdapterList, méthode

Génère une liste d’objets adaptateur représentant l’état actuel de l’adaptateur du système et répondant aux critères spécifiés. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a>Paramètres

### <a name="numattributes"></a>numAttributes

Type : **uint32_t**

Nombre d’éléments dans le tableau vers lequel pointe l’argument *FilterAttributes* .

### <a name="filterattributes-in"></a>filterAttributes [in]

Type : **const GUID \***

Pointeur vers un tableau de GUID d’attribut d’adaptateur. Pour obtenir la liste des GUID d’attribut, consultez [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md). Au moins un GUID doit être fourni. Dans le cas où plusieurs GUID sont fournis dans le tableau, seuls les adaptateurs qui satisfont à *tous* les attributs demandés sont inclus dans la liste retournée.

### <a name="riid"></a>riid

Type : **REFIID**

Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvAdapterList*. Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).

### <a name="ppvadapterlist-out"></a>ppvAdapterList [out]

Type : **void \* \***

Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* . Une fois le retour réussi, *\* ppvAdapterList* (l’adresse déréférencée) contient un pointeur vers la liste d’adaptateurs créée.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur retournée|Description|
|-|-|
|E_INVALIDARG|`nullptr` a été fourni pour *FilterAttributes*, ou 0 a été fourni pour *numAttributes*.|
|E_NOINTERFACE|Une valeur non valide a été fournie pour *riid*.|
|E_POINTER|`nullptr` a été fourni pour *ppvAdapterList*.|

## <a name="remarks"></a>Notes

Même si aucun adaptateur n’est trouvé, à condition que les arguments soient valides, **CreateAdapterList** crée un objet [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) valide et retourne **S_OK**. Une fois générés, les adaptateurs de cette liste spécifique ne sont pas modifiés. Toutefois, la liste est considérée comme obsolète si l’un des adaptateurs devient non valide, ou si un nouvel adaptateur répond aux critères de filtre fournis. La liste retournée par **CreateAdapterList** n’est pas ordonnée d’une manière particulière, mais l’ordre d’une liste est cohérent entre plusieurs appels, et même entre les redémarrages du système d’exploitation. Le classement peut changer lors des modifications de configuration du système, y compris l’ajout ou la suppression d’un adaptateur, ou la mise à jour d’un pilote sur un adaptateur existant. Vous pouvez vous inscrire à ces modifications avec [IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) en utilisant le type de notification **DXCoreNotificationType. AdapterListStale**.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)