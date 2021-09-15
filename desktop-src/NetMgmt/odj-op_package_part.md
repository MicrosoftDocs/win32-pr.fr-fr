---
title: OP_PACKAGE_PART
description: Définition du OP_PACKAGE_PART IDL
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517741"
---
# <a name="op_package_part-structure"></a>Structure OP_PACKAGE_PART

Définit une structure qui contient un jeu de données identifié par un GUID.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a>Membres

### <a name="parttype"></a>PartType

Identifie la structure sérialisée contenue dans la partie en fonction du tableau suivant :

|PartType|Signification|
| --- | --- |
|GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}|Contient une structure ODJ_WIN7_BLOB sérialisée.|
|GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}|Contient une structure OP_JOIN_PROV2_PART sérialisée.|
|GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}|Contient une structure OP_JOIN_PROV3_PART sérialisée.|
|GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}|Contient une structure OP_CERT_PART sérialisée.|
|GUID_POLICY_PROVIDER {68fb602a-0c09-48CE-b75f-07b7bd58f7ec}|Contient une structure OP_POLICY_PART sérialisée.|

### <a name="ulflags"></a>ulFlags

Doit être défini sur zéro, un ou plusieurs des indicateurs suivants :

|Valeur|Signification|
| --- | --- |
|OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)|Cette partie de package est considérée comme essentielle. Si le consommateur ne reconnaît pas ce composant de package ou ne parvient pas à le traiter correctement, l’opération globale doit échouer.|

### <a name="part"></a>Partie

Contient une structure sérialisée dans une structure OP_BLOB. La structure spécifique est déterminée par PartType.

### <a name="extension"></a>Extension

Réservé pour une utilisation ultérieure et doit être défini sur tous les zéros.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_objet BLOB op**](odj-op_blob.md)
