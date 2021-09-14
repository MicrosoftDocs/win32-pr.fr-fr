---
description: Détermine si les paramètres régionaux spécifiés par le nom sont installés ou pris en charge sur le système d’exploitation.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: RtlIsValidLocaleName, fonction (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121894"
---
# <a name="rtlisvalidlocalename-function"></a>RtlIsValidLocaleName fonction)

Détermine si les paramètres régionaux spécifiés par le nom sont installés ou pris en charge sur le système d’exploitation.

> [!Note]  
> cette fonction peut être utilisée uniquement dans Windows Vista. Il peut être modifié ou non disponible dans les versions ultérieures. Les applications doivent utiliser [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LocaleName* \[ dans\]
</dt> <dd>

[Nom des paramètres régionaux](locale-names.md) à valider. Ce paramètre peut spécifier le nom des [paramètres régionaux personnalisés](custom-locales.md).

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Indicateurs indiquant si les paramètres régionaux neutres sont considérés comme valides. Actuellement, la seule option définie pour les [paramètres régionaux \_ autorise le \_ neutre](locale-allow-neutral.md). La valeur par défaut est qu’ils ne le sont pas.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou 0 dans le cas contraire.

## <a name="remarks"></a>Notes

Cette fonction est similaire à [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename). La seule différence réside dans le fait que si les paramètres régionaux \_ autorisent la \_ neutralité est défini, **RtlIsValidLocaleName** retourne la **valeur true** pour un nom qui correspond à des paramètres régionaux neutres (par exemple, « en »), tandis que [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) retourne **true** uniquement pour des paramètres régionaux spécifiques (tels que « en-US »). les paramètres régionaux neutres sont utilisés dans le cadre de la stratégie de chargement des ressources dans Windows Vista et versions ultérieures. Seule une petite classe d’applications hautement spécialisées utilise **RtlIsValidLocaleName** et Set locale \_ autorisent la \_ neutralité, car les paramètres régionaux neutres sont très peu utilisés. Aucune des fonctions décrites dans [appel des fonctions « nom des paramètres régionaux »](calling-the--locale-name--functions.md) n’accepte les paramètres régionaux neutres en tant qu’entrées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Ntrtl. h</dt> </dl>      |
| Bibliothèque<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des langues nationales](national-language-support.md)
</dt> <dt>

[Fonctions de prise en charge linguistique nationale](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




