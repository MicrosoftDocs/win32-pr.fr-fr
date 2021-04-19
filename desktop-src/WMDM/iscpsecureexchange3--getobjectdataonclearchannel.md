---
title: Méthode GetObjectDataOnClearChannel
description: La méthode GetObjectDataOnClearChannel transfère à Windows Media Gestionnaire de périphériques un bloc de données d’objet sur un canal clair.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Méthode GetObjectDataOnClearChannel Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535227"
---
# <a name="getobjectdataonclearchannel-method"></a>Méthode GetObjectDataOnClearChannel

La méthode **GetObjectDataOnClearChannel** transfère à Windows Media gestionnaire de périphériques un bloc de données d’objet sur un canal clair.

Cette méthode est identique à [**ISCPSecureExchange :: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , sauf que les données retournées par cette méthode ne sont pas chiffrées. Par conséquent, cette méthode est plus efficace.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* 
</dt> <dd>

Pointeur vers l’objet appareil.

</dd> <dt>

*pData* 
</dt> <dd>

Pointeur vers une mémoire tampon destinée à recevoir des données.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Pointeur vers une **valeur DWORD** contenant la taille de transfert.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. Si la méthode échoue, elle retourne un code d’erreur **HRESULT** .



| Code de retour                                                                                                | Description                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**échec de la vérification de WMDM \_ E \_ Mac \_ \_**</dt> </dl> | Le code d’authentification du message n’est pas valide.<br/>                                    |
| <dl> <dt>**WMDM \_ E \_ nojustes**</dt> </dl>           | L’appelant ne dispose pas des droits nécessaires pour effectuer l’opération demandée.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Échec de la méthode. Arrêtez l’interaction avec le fournisseur de contenu.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Un paramètre est un pointeur **null** ou non valide.<br/>                                   |
| <dl> <dt>**E \_ échec**</dt> </dl>                     | Une erreur non spécifiée s'est produite.<br/>                                                   |



 

## <a name="remarks"></a>Notes

Pour transférer des données, Windows Media Gestionnaire de périphériques appelle la méthode [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) pour obtenir les données du conteneur. **GetObjectDataOnClearChannel** est ensuite appelé pour transférer des blocs de données d’objet du fournisseur de contenu vers Windows Media gestionnaire de périphériques. Si l' \_ opération S OK est retournée avec *pdwSize* défini à zéro, Windows Media gestionnaire de périphériques demandera aucune autre donnée.

Cette méthode est identique à [**ISCPSecureExchange :: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , sauf que les données retournées par cette méthode ne sont pas chiffrées. Par conséquent, cette méthode est plus efficace.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMSCP. idl</dt> </dl>    |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCPSecureExchange :: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Interface ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





