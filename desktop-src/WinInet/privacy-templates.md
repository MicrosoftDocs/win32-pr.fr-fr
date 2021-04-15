---
title: Modèles de confidentialité (Wininet. h)
description: Voici des niveaux de confidentialité qui correspondent aux règles d’acceptation, d’acceptation ou de refus conditionnel des cookies.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9394068721920836f61871ca42471469fd4c592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467010"
---
# <a name="privacy-templates"></a>Modèles de confidentialité

Voici des niveaux de confidentialité qui correspondent aux règles d’acceptation, d’acceptation ou de refus conditionnel des cookies. Ces niveaux correspondent aux niveaux de préférences de confidentialité définis sous l’onglet confidentialité dans Options Internet. Pour plus d’informations sur les définitions, consultez [confidentialité dans Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) .

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**modèle de confidentialité \_ \_ aucun \_ cookie**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Cela revient à **bloquer tous les cookies** sur la barre de curseur des préférences de confidentialité dans les **Options Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**modèle de confidentialité \_ \_ élevé**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Cela est **identique à celui** de la barre de défilement des préférences de confidentialité dans les **Options Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**modèle de confidentialité \_ \_ moyen \_ élevé**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



C’est le même que **le \_ niveau moyen élevé** sur la barre de curseur des préférences de confidentialité dans les **Options Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**modèle de confidentialité \_ \_ moyen**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



C’est la même chose que la **moyenne** sur la barre du curseur des préférences de confidentialité dans **Options Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**modèle de confidentialité \_ \_ moyen \_ faible** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Cela est identique à celui **de la barre de défilement** des préférences de confidentialité dans les **Options Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**modèle de confidentialité \_ \_ faible**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Cela revient à **accepter tous les cookies** sur la barre de curseur des préférences de confidentialité dans les **Options Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**modèle de confidentialité \_ \_ personnalisé**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Défini par l’utilisateur. Consultez [comment créer un fichier d’importation de confidentialité personnalisé](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) pour comprendre comment définir des paramètres de confidentialité personnalisés.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**modèle de confidentialité \_ \_ avancé**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Défini par l’utilisateur. Les options avancées sont définies dans la boîte de dialogue **paramètres de confidentialité avancés** accessible à partir de l’onglet **confidentialité** dans **Options Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**modèle de confidentialité \_ \_ Max.**
</dt> <dd> <dl> <dt>

modèle de confidentialité \_ \_ faible
</dt> <dt>



Identique au **modèle de confidentialité \_ \_ faible**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

