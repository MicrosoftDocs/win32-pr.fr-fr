---
description: La \_ classe CIM SupportAccess définit comment obtenir de l’aide pour un produit.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: Classe CIM_SupportAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c53254b51b228efb2c1f14b7fb5f07475fb275d20c7df6444dc88e048bb1d30f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020907"
---
# <a name="cim_supportaccess-class"></a>\_Classe CIM SupportAccess

La classe **CIM \_ SupportAccess** définit comment obtenir de l’aide pour un produit.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SupportAccess** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SupportAccess** possède les propriétés suivantes.

<dl> <dt>

**CommunicationInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU DMTF \| 002,11 "," MIF. \|FRU DMTF \| 002,12 ")
</dt> </dl>

Détails du mode de communication. par exemple, si la propriété **CommunicationMode** est « Téléphone », cette propriété spécifie le numéro de téléphone à appeler.

</dd> <dt>

**CommunicationMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Support \| 001,5»)
</dt> </dl>

Forme de communication à utiliser pour obtenir un support.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Téléphone** (2)


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Télécopie** (3)


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span id="BBS"></span><span id="bbs"></span>**BBS** (4)


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Service en ligne** (5)


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Page Web** (6)


</dt> <dd>

Page web

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span id="FTP"></span><span id="ftp"></span>**FTP** (7)


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**Courrier électronique** (8)


</dt> <dd>

E-mail

</dd> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Support \| 001,3»)
</dt> </dl>

Description textuelle du type de prise en charge fourni.

</dd> <dt>

**Paramètres régionaux**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Support \| 001,2 "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

La région géographique ou le dialecte de langage auquel cette ressource de support appartient.

</dd> <dt>

**SupportAccessId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Chaîne de forme libre arbitraire définie par le fournisseur du produit ou par l’organisation qui déploie le produit. Dans la mesure où il s’agit d’une clé, cette propriété doit être unique dans toute l’entreprise.

</dd> </dl>

## <a name="remarks"></a>Remarques

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

