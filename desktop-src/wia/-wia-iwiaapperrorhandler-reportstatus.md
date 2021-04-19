---
description: Gère l’état des appareils et les messages d’erreur pendant les transferts de données d’image et affiche les messages à l’utilisateur.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'IWiaAppErrorHandler :: ReportStatus, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533762"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>IWiaAppErrorHandler :: ReportStatus, méthode

Gère l’état des appareils et les messages d’erreur pendant les transferts de données d’image et affiche les messages à l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Non utilisé. Définit la valeur 0.

</dd> <dt>

*pWiaItem2* \[ dans\]
</dt> <dd>

Tapez : **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Pointeur vers l’élément en cours de transfert.

</dd> <dt>

_hrStatus * \[ dans\]
</dt> <dd>

Type : **HRESULT**

Code d’état de l’appareil.

</dd> <dt>

*lPercentComplete* \[ dans\]
</dt> <dd>

Type : **long**

Pourcentage effectué de l’opération en cours.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Retourne *hrStatus* si la récupération à partir de l’erreur n’est pas possible. Dans le cas contraire, elle retourne l’une des valeurs suivantes.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Si *hrStatus* est une erreur, l’action appropriée a été effectuée pour corriger l’erreur et le transfert peut continuer. Si *hrStatus* est informatif, l’utilisateur a été informé avec une boîte de dialogue non modale et a choisi de ne pas annuler le transfert.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                  | L’utilisateur a annulé le transfert à partir de la boîte de dialogue non modale du gestionnaire d’erreurs. Cette valeur peut être retournée à n’importe quel point, quelle que soit la valeur de l’élément *hrStatus* . <br/>                                                                                      |
| <dl> <dt>**\_État WIA \_ non \_ géré**</dt> </dl> | Aucune action n’a été effectuée ; autrement dit, aucune boîte de dialogue n’a été présentée à l’utilisateur. Le gestionnaire d’erreurs suivant sera appelé. L’ordre des gestionnaires d’erreurs est le suivant : application, pilote et système par défaut.<br/>                                                 |



 

## <a name="remarks"></a>Notes

Le paramètre *lPercentComplete* permet à une fenêtre de gestionnaire d’erreurs d’afficher la progression. Par exemple, un pilote peut fournir une estimation du temps nécessaire à la mise en route. Le paramètre *lPercentComplete* passé dans **IWiaAppErrorHandler :: ReportStatus** est la même valeur que le **lPercentComplete** que le pilote définit dans la structure [**WiaTransferParams**](-wia-wiatransferparams.md) .

Un gestionnaire d’erreurs peut utiliser les macros ayant réussi et échoué pour déterminer si *hrStatus* a une erreur de gravité \_ ou une gravité de gravité \_ .

Si le niveau de gravité de la valeur de *hrStatus* est \_ réussite, l’utilisateur doit être autorisé à annuler le transfert.

Si *hrStatus* est \_ une erreur de gravité, le gestionnaire d’erreurs doit afficher une boîte de dialogue modale détenue par la fenêtre parente de l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




