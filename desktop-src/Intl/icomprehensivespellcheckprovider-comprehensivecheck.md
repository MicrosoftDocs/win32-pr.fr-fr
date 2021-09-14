---
description: 'Vérifiez l’orthographe du texte du fournisseur de manière plus approfondie que ISpellCheckProvider :: Check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'IComprehensiveSpellCheckProvider :: ComprehensiveCheck, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240275"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>IComprehensiveSpellCheckProvider :: ComprehensiveCheck, méthode

Vérifiez l’orthographe du texte du fournisseur de manière plus approfondie que [**ISpellCheckProvider :: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*texte* \[ dans\]
</dt> <dd>

Texte à vérifier.

</dd> <dt>

*résultat* \[ à\]
</dt> <dd>

Résultat de la vérification de ce texte, sous la forme d’une énumération des fautes d’orthographe ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), le cas échéant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur de retour                                                                             | Description                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>\_OK</dt> </dl>         | Vendu.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | le *texte* est une chaîne vide.<br/> |
| <dl> <dt>\_pointeur E</dt> </dl>    | le *texte* est un pointeur null.<br/>  |



 

## <a name="remarks"></a>Notes

Cette interface n’est pas obligatoire pour être implémentée par un fournisseur de vérification orthographique. Toutefois, si le fournisseur prend en charge deux « modes » de vérification orthographique (plus rapide et plus rapide, mais plus complet), il doit implémenter cette interface dans le même objet qui implémente [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) pour prendre en charge le mode de vérification plus approfondi. Lorsqu’un client appelle [**des :: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la fonctionnalité de vérification orthographique effectue une opération [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour le fournisseur de [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)et appelle **IComprehensiveSpellCheckProvider. ComprehensiveCheck** si l’interface est prise en charge. Si l’interface n’est pas prise en charge, elle revient silencieusement à [**ISpellCheckProvider :: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**Des :: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider :: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
