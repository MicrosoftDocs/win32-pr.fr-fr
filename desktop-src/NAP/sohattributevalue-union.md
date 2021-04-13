---
title: SoHAttributeValue Union (NapProtocol. h)
description: Définit le contenu du membre de type dans une structure SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- SoHAttributeValue d’Union NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466458"
---
# <a name="sohattributevalue-union"></a>SoHAttributeValue Union

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’Union **SoHAttributeValue** définit le contenu du membre de **type** dans une structure [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) . La structure de l’Union **SoHAttributeValue** est déterminée par le [**SoHAttributeType**](sohattributetype-enum.md) spécifié dans le membre de **type** de la structure [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .

## <a name="syntax"></a>Syntaxe


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a>Membres

<dl> <dt>

**idVal**
</dt> <dd>

**cas (sohAttributeTypeSystemHealthId)**

[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent d’intégrité système (SHA) ou du programme de validation d’intégrité système (SHV) qui a construit ce paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

**v4AddressesVal**
</dt> <dd>

**cas (sohAttributeTypeIpv4FixupServers)**

Les adresses IPv4 des serveurs de correction utilisés par le système NAP.

<dl> <dt>

**count**
</dt> <dd>

Nombre d’adresses IPv4 dans le membre **Addresses** dans la plage comprise entre 1 et [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**addresses**
</dt> <dd>

Tableau de structures [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) qui contiennent les adresses IPv4.

</dd> </dl> </dd> <dt>

**v6AddressesVal**
</dt> <dd>

**cas (sohAttributeTypeIpv6FixupServers)**

Les adresses IPv6 des serveurs de correction utilisés par le système NAP.

<dl> <dt>

**count**
</dt> <dd>

Nombre d’adresses IPv4 dans le membre **Addresses** dans la plage comprise entre 1 et [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**addresses**
</dt> <dd>

Tableau de structures [**AdresseIPv6**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) qui contiennent les adresses IPv4.

</dd> </dl> </dd> <dt>

**codesVal**
</dt> <dd>

**case (sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**

Structure [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) qui contient les codes de résultat de conformité de l’application définis pour les [**constantes d’erreur**](nap-error-constants.md)de client ou NAP. Un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) doit contenir ce TLV ou le **sohAttributeTypeFailureCategory** TLV.

</dd> <dt>

**dateTimeVal**
</dt> <dd>

**case (sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**

Structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui contient l’heure de la dernière mise à jour de [**déclaration d’intégrité**](/windows/win32/api/naptypes/ns-naptypes-soh) ou la durée de génération de **déclaration d’intégrité** .

</dd> <dt>

**vendorSpecificVal**
</dt> <dd>

**cas (sohAttributeTypeVendorSpecific)**

Données spécifiques à l’application définies par le fournisseur.

<dl> <dt>

**vendorId**
</dt> <dd>

Identificateur de 4 octets qui définit l’ID de la paire SHA/SHV. Les 3 premiers octets correspondent au code SMI attribué par l’IETF au fournisseur et le dernier octet identifie le composant lui-même. Lors de l’implémentation d’un SHA ou d’un SHV, n’utilisez pas les valeurs d’ID attribuées aux composants d’intégrité système Microsoft internes sur les [**constantes de fournisseur NAP**](nap-vendor-constants.md).

</dd> <dt>

**size**
</dt> <dd>

Taille, en octets, des données de fournisseur dans la plage comprise entre 0 et ([**maxSoHAttributeSize**](nap-type-constants.md) -4).

</dd> <dt>

**Champ vendorspecificdata**
</dt> <dd>

Pointeur vers les données spécifiques au fournisseur dans l’ordre des octets du réseau.

</dd> </dl> </dd> <dt>

**uint8Val**
</dt> <dd>

**case (sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory, sohAttributeTypeExtendedIsolationState)**

La classe d’intégrité, la catégorie d’échec ou l’état d’isolement étendu d’un composant NAP en tant que valeur [**HealthClassValue**](healthclassvalue-enum.md) ou [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) , ou une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .

</dd> <dt>

**octetStringVal**
</dt> <dd>

**default**

Les valeurs des attributs suivants sont des chaînes d’octets :

-   sohAttributeTypeSoftwareVersion
-   sohAttributeTypeClientId
-   sohAttributeTypeProductName
-   sohAttributeTypeHealthClassStatus

Pour la compatibilité ascendante, tous les attributs non reconnus sont retournés en tant que chaînes d’octets. les **données** doivent être dans l’ordre des octets du réseau.

<dl> <dt>

**size**
</dt> <dd>

Taille, en octets, des **données** dans la plage comprise entre 0 et [**maxSoHAttributeSize**](nap-type-constants.md).

</dd> <dt>

**data**
</dt> <dd>

Pointeur vers la valeur de chaîne d’octets.

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a>Disposition réelle des données

En raison de la nature de l’environnement de publication du SDK, les unions ne sont pas clairement représentées dans les blocs de syntaxe. Voici la syntaxe réelle du fichier d’en-tête NapProtocol. h.


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a>Notes

Ces types d’attributs sont consommés par le système NAP :

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

Le reste du [**SoHAttributeTypes**](sohattributetype-enum.md) est conçu de manière purement normative pour une utilisation par les programmes d’intégrité des intégrité et les SHV.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence NAP](nap-reference.md)
</dt> <dt>

[Structures NAP](nap-structures.md)
</dt> </dl>

 

