---
description: Définit un cache de métriques de police Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4376f0b69de8d9e963cae6a156eff8c3724ac375db3c18bce0a80855afd6f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130239"
---
# <a name="script_cache"></a>CACHE de SCRIPT \_

Définit un cache de métriques de police Uniscribe.


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>Remarques

Il s’agit d’une structure opaque. L’application doit allouer et conserver une \_ variable de cache de script pour chaque style de caractère utilisé. La variable doit être initialisée avec la **valeur null**.

De nombreuses fonctions de script prennent une combinaison d’un handle de contexte de périphérique matériel et d’une variable de cache de SCRIPT \_ . Uniscribe tente d’abord d’accéder aux données de police à l’aide de la \_ variable cache de script. Il inspecte uniquement le contexte de périphérique matériel si les données requises ne sont pas déjà mises en cache.

Le descripteur de contexte de périphérique matériel peut être passé à Uniscribe en tant que **valeur null**. Si les données requises par Uniscribe sont déjà mises en cache, le contexte de périphérique n’est pas accessible et l’opération se poursuit normalement.

Si le contexte de périphérique est passé comme **null** et que Uniscribe doit y accéder pour une raison quelconque, Uniscribe retourne le code d’erreur E \_ en attente. Ce code est retourné rapidement, ce qui permet à l’application d’éviter les appels [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) fastidieux.

## <a name="examples"></a>Exemples

L’exemple suivant s’applique à toutes les fonctions qui prennent une variable de cache de SCRIPT \_ et un handle facultatif à un contexte de périphérique matériel.


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Structures Uniscribe](uniscribe-structures.md)
</dt> <dt>

[Mise en cache](caching.md)
</dt> </dl>

 

 
