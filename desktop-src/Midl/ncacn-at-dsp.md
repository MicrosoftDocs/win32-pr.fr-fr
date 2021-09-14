---
title: attribut ncacn_at_dsp
description: Le \_ \_ mot clé ncacn at DSP identifie le DSP AppleTalk comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093382"
---
# <a name="ncacn_at_dsp-attribute"></a>ncacn \_ au niveau de l' \_ attribut DSP

Le mot clé **ncacn \_ at \_ DSP** identifie le DSP AppleTalk comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du port* 
</dt> <dd>

Spécifie une chaîne de caractères d’une longueur maximale de 22 octets.

</dd> </dl>

## <a name="remarks"></a>Notes

La syntaxe de la chaîne de port DSP AppleTalk, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL. Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**liaison de chaîne**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 