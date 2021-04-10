---
title: Méthodes de propriété IADsNameTranslate (IADs. h)
description: Définit la propriété ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsNameTranslate ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942567"
---
# <a name="iadsnametranslate-property-methods"></a>Méthodes de propriété IADsNameTranslate

La méthode Property de l’interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) définit la propriété **ChaseReferral** . Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**ChaseReferral**
</dt> <dd> <dl>

Options de repérage de références telles qu’elles sont définies dans l' [**\_ \_ \_ énumération des références de la Chase ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum). Lorsque le repérage de références est défini, la traduction de nom est effectuée sur les objets qui n’appartiennent pas à ce répertoire et les références retournées par le repérage de références.

<dt>

Type d’accès : écriture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Notes

Les options de repérage de références s’appliquent uniquement lorsque vous utilisez [**IADsNameTranslate :: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) et [**IADsNameTranslate :: obten**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get). La fonctionnalité n’est pas disponible avec [**IADsNameTranslate :: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) ou [**IADsNameTranslate :: GETEX**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).

L’interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) a une implémentation partielle de [**l' \_ \_ \_ énumération de références de la Chase ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) par le biais de la propriété **ChaseReferral** . Si la propriété **ChaseReferral** a la valeur zéro (0), elle est identique à la spécification des références de la **Chase des publicités \_ \_ \_ jamais** (0). Si une valeur différente de zéro est utilisée, elle est identique à la spécification des références de la **Chase des publicités \_ \_ \_ Always** (0x60). **IADsNameTranslate** n’implémente pas les options de **\_ références de poursuites ad \_ \_ subordonnées** (0x20) ou de références de la **\_ Chase ADS \_ \_ externes** (0x40).

Le paramètre par défaut pour le repérage de références est activé (les références de la **poursuite ADS sont \_ \_ \_ toujours**). Sans le repérage de références, vous pouvez faire en sorte que la traduction de noms soit effectuée sur les objets résidant uniquement sur le serveur d’annuaire connecté. Si vous n’êtes pas certain que l’objet concerné se trouve sur le serveur spécifié, vous devez définir cette propriété sur les références de la **\_ Chase ADS \_ \_ Always**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate est défini en tant que B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ énumérations de références de Chase ADS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate :: obtient**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate :: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Méthodes de propriété d’interface](interface-property-methods.md)
</dt> </dl>

 

 





