---
title: Decode, attribut
description: L’attribut \ Decode \ ACF spécifie qu’une procédure ou un type a besoin d’une prise en charge de la désérialisation.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Decoded, attribut MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093689"
---
# <a name="decode-attribute"></a>Decode, attribut

L’attribut **\[ Decode \]** ACF spécifie qu’une procédure ou un type a besoin d’une prise en charge de la désérialisation.

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs qui s’appliquent à l’ensemble de l’interface.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*définition d’interface* 
</dt> <dd>

Spécifie les instructions IDL qui forment la définition de l’interface.

</dd> <dt>

*op-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs opérationnels qui s’appliquent à la procédure, tels que **\[** [**encode**](encode.md) **\]** .

</dd> <dt>

*nom de la procédure* 
</dt> <dd>

Spécifie le nom de la procédure.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs, tels que **\[** [**encode**](encode.md) **\]** et **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*nom du type* 
</dt> <dd>

Spécifie un type défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ Decode \]** fait en sorte que le compilateur MIDL génère du code qu’une application peut utiliser pour récupérer des données sérialisées à partir d’une mémoire tampon. L' **\[** attribut [**encode**](encode.md) **\]** fournit la prise en charge de la sérialisation, en générant le code permettant de sérialiser les données dans une mémoire tampon.

Utilisez les **\[** [](encode.md) **\]** attributs encode et **\[ Decode \]** dans un CCP pour générer le code de sérialisation des procédures ou des types définis dans le fichier IDL d’une interface. Lorsqu’il est utilisé comme attribut d’interface, **\[ Decode \]** s’applique à tous les types et procédures définis dans le fichier IDL. En cas d’utilisation comme attribut de type, **\[ Decode \]** s’applique uniquement au type spécifié. En cas d’utilisation comme attribut opérationnel, **\[ Decode \]** s’applique uniquement à cette procédure.

Pour plus d’informations sur l’utilisation de cette prise en charge de la sérialisation, consultez [services de sérialisation](/windows/desktop/Rpc/serialization-services) et **\[** [**encodage**](encode.md) **\]** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**lui**](allocate.md)
</dt> <dt>

[**contraire**](encode.md)
</dt> </dl>

 

 