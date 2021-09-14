---
description: Les \_ constantes d’indicateur de bit LINESPECIALINFO décrivent des signaux d’information spéciaux que le réseau peut utiliser pour signaler diverses opérations de rapports et d’observation du réseau.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Constantes LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324700"
---
# <a name="linespecialinfo_-constants"></a>\_Constantes LINESPECIALINFO

Les constantes d’indicateur de bit **LINESPECIALINFO \_** décrivent des signaux d’information spéciaux que le réseau peut utiliser pour signaler diverses opérations de rapports et d’observation du réseau. Il s’agit de séquences de fréquences codées spéciales transmises au début des annonces enregistrées de l’avis réseau.

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**
</dt> <dd> <dl> <dt>



Ce titre d’information spécial précède un nombre vacant, AIS, un changement de numéro Centrex et une station chômée, le code d’accès n’est pas composé ou composé d’erreurs ou le message d’opérateur d’interception manuelle (catégorie d’irrégularité du client). LINESPECIALINFO \_ CUSTIRREG est également signalé lorsque les informations de facturation sont rejetées et lorsque l’adresse composed est bloquée au niveau du commutateur.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuit**
</dt> <dd> <dl> <dt>



Ce titre d’information spécial précède un circuit non ou une annonce d’urgence (catégorie de blocage de troncation).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**réorganisation LINESPECIALINFO \_**
</dt> <dd> <dl> <dt>



Ce titre d’information spécial précède une annonce de réorganisation (catégorie d’irrégularité d’équipement). \_La réorganisation LINESPECIALINFO est également signalée lorsque le téléphone est maintenu offhook trop long.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO \_ INdispo**
</dt> <dd> <dl> <dt>



Les spécificités relatives à la tonalité des informations spéciales ne sont pas disponibles et ne seront pas connues.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ inconnu**
</dt> <dd> <dl> <dt>



Les spécificités relatives à la tonalité des informations spéciales sont actuellement inconnues, mais peuvent devenir connues plus tard.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Des tonalités spéciales sont définies pour les messages de notification et ne sont généralement pas utilisées à des fins de facturation ou de supervision.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




