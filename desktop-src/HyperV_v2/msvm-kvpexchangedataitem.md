---
description: Représente une paire clé/valeur.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Classe Msvm_KvpExchangeDataItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529438"
---
# <a name="msvm_kvpexchangedataitem-class"></a>MSVM \_ KvpExchangeDataItem, classe

Représente une paire clé/valeur.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ KvpExchangeDataItem** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ KvpExchangeDataItem** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Données**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Partie valeur de la paire clé/valeur.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Partie clé de la paire clé/valeur.



| Clé                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"CSDVersion"</dt> </dl>                 | Chaîne qui représente le dernier Service Pack installé sur le système invité. Par exemple, « Service Pack 2 ». Si aucun Service Pack n’a été installé, cette chaîne est vide.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>FullyQualifiedDomainName</dt> </dl>   | Chaîne qui représente le nom DNS complet qui identifie de façon unique l’ordinateur local. Ce nom est une combinaison du nom d’hôte DNS et du nom de domaine DNS, en utilisant *le format nom d’hôte.* *Nom_domaine*. Si l’ordinateur local est un nœud dans un cluster, cette valeur est le nom DNS complet du serveur virtuel de cluster. Cette valeur correspond au nom retourné par la fonction [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) lorsque le paramètre *NameType* est « ComputerNameDnsFullyQualified ».<br/> |
| <dl> <dt>"IntegrationServicesVersion"</dt> </dl> | Chaîne représentant la version de la Integration Services actuellement installée sur la machine virtuelle invitée (par exemple, « 6.1.7000.0 »).<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"NetworkAddressIPv4"</dt> </dl>         | Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv4 actuellement affectées à la machine virtuelle invitée. La liste est automatiquement mise à jour chaque fois qu’une modification de configuration TCP/IP se produit sur la machine virtuelle invitée. Chaque adresse est représentée sous la forme d’une notation décimale à points. <br/>                                                                                                                                                                                                                         |
| <dl> <dt>"NetworkAddressIPv6"</dt> </dl>         | Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv6 actuellement affectées à la machine virtuelle invitée. La liste est automatiquement mise à jour chaque fois qu’une modification de configuration TCP/IP se produit sur la machine virtuelle invitée. Chaque adresse est représentée en notation hexadécimale à deux-points. Il n’est pas garanti que les listes IPv4 et IPv6 soient synchronisées à tout moment.<br/>                                                                                                                                             |
| <dl> <dt>"OSBuildNumber"</dt> </dl>              | Chaîne qui représente le numéro de build du système d’exploitation.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"OSEditionId"</dt> </dl>                | Chaîne représentant l’édition (SKU) du système d’exploitation de la machine virtuelle invitée. Pour obtenir la liste des valeurs possibles, consultez la fonction [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>OSName</dt> </dl>                     | Chaîne qui représente le nom du système d’exploitation. Cette valeur provient de l’entrée de Registre suivante : **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**<br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <dt>OSMajorVersion</dt> </dl>             | Chaîne qui représente le numéro de version principale du système d’exploitation.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>OSMinorVersion</dt> </dl>             | Chaîne qui représente le numéro de version mineure du système d’exploitation.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSPlatformId"</dt> </dl>               | Chaîne qui représente la plateforme du système d’exploitation. Les valeurs possibles de la propriété de **données** sont « 1 » pour indiquer un système Windows non pris en charge et « 2 » pour indiquer un système Windows pris en charge.<br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>OSVersion</dt> </dl>                  | Chaîne qui représente la version du système d’exploitation. Le format de cette chaîne est *MajorVersion*. *MinorVersion*. *BuildNumber*. Par exemple, « 5.2.3790 » pour Windows Server 2003.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>ProcessorArchitecture</dt> </dl>      | Chaîne qui représente l’architecture du processeur du système d’exploitation. Pour obtenir la liste des valeurs, consultez le membre **wProcessorArchitecture** de la structure des [**\_ informations système**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .<br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>ProductType</dt> </dl>                | Chaîne qui représente le type de produit. Pour obtenir la liste des valeurs, consultez le membre **wProductType** de la structure [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"RDPAddressIPv4"</dt> </dl>             | Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv4 que la pile RDP de l’ordinateur virtuel invité écoute actuellement. Si la pile RDP n’est pas en cours d’exécution, la chaîne est vide. La liste est automatiquement mise à jour chaque fois qu’une modification de la configuration TCP/IP affecte la pile RDP sur la machine virtuelle invitée. Chaque adresse est représentée sous la forme d’une notation décimale à points.<br/>                                                                                                                   |
| <dl> <dt>"RDPAddressIPv6"</dt> </dl>             | Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv6 sur lesquelles la pile RDP d’ordinateur virtuel invité écoute actuellement. Si la pile RDP n’est pas en cours d’exécution, la chaîne est vide. La liste est automatiquement mise à jour chaque fois qu’une modification de la configuration TCP/IP affecte la pile RDP sur la machine virtuelle invitée. Chaque adresse est représentée en notation hexadécimale à deux-points.<br/>                                                                                                             |
| <dl> <dt>"ServicePackMajor"</dt> </dl>           | Chaîne qui représente le numéro de version principale du dernier Service Pack installé sur le système.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"ServicePackMinor"</dt> </dl>           | Chaîne qui représente le numéro de version mineure de la dernière Service Pack installée sur le système.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"SuiteMask"</dt> </dl>                  | Chaîne qui représente les suites de produits disponibles sur le système. Cette chaîne est une combinaison de l’une des valeurs du membre **wSuiteMask** de la structure [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Source**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Source des données.



| Valeur                                                                        | Signification                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | « HostExchangeItems » en cas de push par l’hôte.<br/>                                                                                                                                                                                      |
| <dl> <dt>1</dt> </dl> | « GuestExchangeItems » en cas de push par l’ordinateur virtuel invité.<br/>                                                                                                                                                                    |
| <dl> <dt>2</dt> </dl> | « GuestIntrinsicExchangeItems » lorsqu’il est automatiquement rempli par la machine virtuelle invitée.<br/>                                                                                                                                          |
| <dl> <dt>4</dt> </dl> | Indique que l’élément est uniquement un hôte et qu’il n’est pas partagé avec l’ordinateur virtuel invité. Utilisé avec la propriété **HostOnlyItems** de la [**classe \_ KvpExchangeComponentSettingData MSVM**](msvm-kvpexchangecomponentsettingdata.md) . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ KvpExchangeDataItem** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Propriété MANAGEDELEMENT CIM**](cim-managedelement.md)
</dt> <dt>

[**\_Propriété MANAGEDELEMENT CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

