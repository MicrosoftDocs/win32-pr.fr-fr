---
description: La méthode de classe WMI EnableStatic active l’adressage TCP/IP statique pour la carte réseau cible. Par conséquent, DHCP pour cette carte réseau est désactivé.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Méthode EnableStatic de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748141"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode EnableStatic de la \_ classe Win32 NetworkAdapterConfiguration

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** active l’adressage TCP/IP statique pour la carte réseau cible. Par conséquent, DHCP pour cette carte réseau est désactivé.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Adresse IP* \[ dans\]
</dt> <dd>

Répertorie toutes les adresses IP statiques pour la carte réseau actuelle.

Exemple : 155.34.22.0.

</dd> <dt>

*Masque_Sous_réseau* \[ dans\]
</dt> <dd>

Les masques de sous-réseau qui complètent les valeurs dans le paramètre *IPAddress* .

Exemple : 255.255.0.0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et tout autre nombre en cas d’erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Exécution réussie, aucun redémarrage requis**
</dt> <dd>

0

Opération réussie, aucun redémarrage n’est nécessaire.

</dd> <dt>

**Achèvement réussi, redémarrage requis**
</dt> <dd>

1

Opération terminée, redémarrage requis.

</dd> <dt>

**Méthode non prise en charge sur cette plateforme**
</dt> <dd>

64

Méthode non prise en charge sur cette plateforme.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

65

Échec inconnu.

</dd> <dt>

**Masque de sous-réseau non valide**
</dt> <dd>

66

Masque de sous-réseau non valide.

</dd> <dt>

**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**
</dt> <dd>

67

Une erreur s’est produite lors du traitement d’une instance qui a été retournée.

</dd> <dt>

**Paramètre d’entrée non valide**
</dt> <dd>

68

Paramètre d’entrée non valide.

</dd> <dt>

**Plus de 5 passerelles spécifiées**
</dt> <dd>

69

Plus de cinq passerelles sont spécifiées.

</dd> <dt>

**Adresse IP non valide**
</dt> <dd>

70

Adresse IP non valide.

</dd> <dt>

**Adresse IP de passerelle non valide**
</dt> <dd>

71

Adresse IP de passerelle non valide.

</dd> <dt>

**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**
</dt> <dd>

72

Une erreur s’est produite lors de l’accès au registre pour les informations demandées.

</dd> <dt>

**Nom de domaine non valide**
</dt> <dd>

73

Nom de domaine non valide.

</dd> <dt>

**Nom d’hôte non valide**
</dt> <dd>

74

Nom d’hôte non valide.

</dd> <dt>

**Aucun serveur WINS principal/secondaire défini**
</dt> <dd>

75

Aucun serveur WINS principal ou secondaire n’est défini.

</dd> <dt>

**Fichier non valide**
</dt> <dd>

76

Fichier non valide.

</dd> <dt>

**Chemin système non valide**
</dt> <dd>

77

Chemin d’accès système non valide.

</dd> <dt>

**Échec de la copie du fichier**
</dt> <dd>

78

Échec de la copie du fichier.

</dd> <dt>

**Paramètre de sécurité non valide**
</dt> <dd>

79

Paramètre de sécurité non valide.

</dd> <dt>

**Impossible de configurer le service TCP/IP**
</dt> <dd>

80

Impossible de configurer le service TCP/IP.

</dd> <dt>

**Impossible de configurer le service DHCP**
</dt> <dd>

81

Impossible de configurer le service DHCP. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**Impossible de renouveler le bail DHCP**
</dt> <dd>

82

Impossible de renouveler le bail DHCP.

</dd> <dt>

**Impossible de libérer le bail DHCP**
</dt> <dd>

83

Impossible de libérer le bail DHCP.

</dd> <dt>

**IP non activé sur l’adaptateur**
</dt> <dd>

84

IP non activé sur l’adaptateur.

</dd> <dt>

**IPX non activé sur l’adaptateur**
</dt> <dd>

85 %

IPX n’est pas activé sur l’adaptateur.

</dd> <dt>

**Erreur liée à un nombre de trames/réseau**
</dt> <dd>

86

Erreur liée à l’image ou au numéro de réseau.

</dd> <dt>

**Type de trame non valide**
</dt> <dd>

87

Type de trame non valide.

</dd> <dt>

**Numéro de réseau non valide**
</dt> <dd>

88

Numéro de réseau non valide.

</dd> <dt>

**Numéro de réseau en double**
</dt> <dd>

89

Numéro de réseau en double.

</dd> <dt>

**Paramètre hors limites**
</dt> <dd>

90

Paramètre hors limites.

</dd> <dt>

**Accès refusé**
</dt> <dd>

91

Accès refusé.

</dd> <dt>

**Mémoire insuffisante**
</dt> <dd>

92

Mémoire insuffisante.

</dd> <dt>

**Existe déjà**
</dt> <dd>

93

Existe déjà.

</dd> <dt>

**Chemin d’accès, fichier ou objet introuvable**
</dt> <dd>

94

Chemin d’accès, fichier ou objet introuvable.

</dd> <dt>

**Impossible de notifier le service**
</dt> <dd>

95

Impossible de notifier le service.

</dd> <dt>

**Impossible d’informer le service DNS**
</dt> <dd>

96

Impossible d’informer le service DNS.

</dd> <dt>

**Interface non configurable**
</dt> <dd>

97

Interface non configurable.

</dd> <dt>

**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**
</dt> <dd>

98

Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.

</dd> <dt>

**DHCP n’est pas activé sur l’adaptateur**
</dt> <dd>

100

DHCP n’est pas activé sur l’adaptateur.

</dd> <dt>

**2147786788**
</dt> <dd>

Verrou d’écriture non activé. Pour plus d’informations, consultez [**INetCfgLock :: AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).

</dd> <dt>

**Autres**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous utilisez **EnableStatic** pour modifier l’adresse IP de l’ordinateur distant, tout en étant connecté via cet adaptateur, vous risquez de perdre la connexion à l’ordinateur distant et de recevoir un message d’erreur RPC non disponible-. (Toutefois, les paramètres sont modifiés). Pour éviter ce scénario, envisagez de modifier la passerelle et/ou les paramètres DNS avant de définir l’adresse IP de la carte.

Lorsque vous utilisez **EnableStatic** pour attribuer à un adaptateur une configuration IP statique, la fonction retourne « 81-impossible de configurer le service DHCP » si la carte est déjà configurée avec une adresse statique. Toutefois, la fonction fonctionne toujours dans le paramètre avec la nouvelle opération.

## <a name="examples"></a>Exemples

L' [adresse IP statique, puis la jointure à un](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) exemple de code PowerShell de domaine, sur la Galerie TechNet, utilise **EnableStatic** pour ajouter une adresse IP statique à un ordinateur local.

L’exemple de code VBScript [attribuer une adresse IP statique](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) , sur la Galerie TechNet, utilise **EnableStatic** pour définir l’adresse IP d’un ordinateur.

L’exemple VBScript suivant montre comment désactiver l’utilisation de DHCP sur une instance de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md). Dans ce cas, nous spécifions l’adaptateur avec un index égal à 0. L’index approprié doit être sélectionné à partir des instances de la carte réseau Win32 \_ pour d’autres interfaces.

> [!Note]  
> Ce script s’applique uniquement aux systèmes basés sur NT modifiez les ipaddr et les variables de sous-réseau ci-dessous en fonction des valeurs que vous souhaitez appliquer à l’adaptateur.

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



L’exemple perl suivant montre comment désactiver l’utilisation de DHCP sur une instance de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md). Dans ce cas, nous spécifions l’adaptateur avec un index égal à 0. L’index approprié doit être sélectionné à partir des instances de la carte réseau Win32 \_ pour d’autres interfaces.

> [!Note]  
> Ce script s’applique uniquement aux systèmes basés sur NT modifiez les ipaddr et les variables de sous-réseau ci-dessous en fonction des valeurs que vous souhaitez appliquer à l’adaptateur.

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tâches WMI : mise en réseau](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tâches WMI : comptes et domaines](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Prise en charge D’ipv6 et IPv6 dans WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

