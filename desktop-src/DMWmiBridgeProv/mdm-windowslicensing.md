---
title: Classe MDM_WindowsLicensing
description: La \_ classe MDM WindowsLicensing est conçue pour les scénarios de gestion des licences.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- Classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, Description
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9470b72cb6a50323af9294be4a6506682fc7aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480925"
---
# <a name="mdm_windowslicensing-class"></a>\_Classe WINDOWSLICENSING MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La classe **MDM \_ WindowsLicensing** est conçue pour les scénarios de gestion des licences. actuellement, l’étendue est limitée aux mises à niveau d’édition de Windows 10 postes de travail et des appareils mobiles, tels que les Windows 10 Professionnel à Windows 10 Entreprise. en outre, ce fournisseur de services cloud offre la possibilité d’activer ou de modifier la clé de produit des appareils Windows 10 desktop.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a>Membres

La **classe \_ WindowsLicensing MDM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MDM \_ WindowsLicensing** possède ces méthodes.




| Méthode | Description | 
|--------|-------------|
| <a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a> | installe une clé de produit pour Windows 10 les appareils de bureau. Ne redémarre pas.<br /> | 
| <a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a> | méthode permettant de vérifier si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit de Windows 10 pour les appareils de bureau.<br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a> | fournissez une licence pour une mise à niveau d’édition de Windows 10 appareils mobiles.<br /><blockquote>[!Note]<br />Ce processus de mise à niveau ne nécessite pas de redémarrage du système.</blockquote><br /><br /> Le type de date est XML.<br /> L’opération prise en charge est Execute.<br /><blockquote>[!Important]<br />le contenu du fichier de licence XML doit être correctement placé dans une séquence d’échappement (c’est-à-dire qu’il ne doit pas simplement être un fichier XML copié), sinon la mise à niveau de l’édition sur Windows 10 appareils mobiles échoue. Pour plus d’informations sur la séquence d’échappement correcte du fichier de licence XML, consultez la section 2,4 de la <a href="https://www.w3.org/TR/xml/">spécification XML du W3C</a>. Le fichier de licence XML est acquis auprès du centre de gestion des licences en volume Microsoft. Votre organisation doit avoir un contrat de licence en volume avec Microsoft pour accéder au portail.</blockquote><br /> Voici les chemins de mise à niveau d’édition valides lors de l’utilisation de ce nœud via un package MDM ou approvisionnement :<ul><li>Windows 10 Mobileto Windows 10 Mobile Entreprise<br /></li></ul><br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a> | Déclenche l’appareil pour prendre la clé de produit et mettre à niveau l’édition du client.<blockquote>[!Note]<br />Ce processus de mise à niveau nécessite un redémarrage du système.</blockquote><br /><br /> L’opération prise en charge est Execute.<br /> Lorsqu’une clé de produit est envoyée d’un serveur MDM à l’appareil d’un utilisateur, <strong>changepk.exe</strong> s’exécute à l’aide de la clé de produit. une fois l’opération terminée, une notification s’affiche pour l’utilisateur qu’une nouvelle édition de Windows 10 est disponible. L’utilisateur peut ensuite redémarrer son système manuellement ou, au bout de deux heures, l’appareil redémarrera automatiquement pour terminer la mise à niveau. L’utilisateur recevra une notification de rappel 10 minutes avant le redémarrage automatique.<br /> Après le redémarrage de l’appareil, le processus de mise à niveau d’édition se termine. L’utilisateur recevra une notification indiquant la réussite de la mise à niveau.<blockquote>[!Important]<br />Si une autre stratégie requiert un redémarrage du système qui se produit lorsque <strong>changepk.exe</strong> est en cours d’exécution, la mise à niveau de l’édition échouera.</blockquote><br /><br /> Si une clé de produit est entrée dans un package de configuration et que l’utilisateur commence l’installation du package, une notification s’affiche pour l’utilisateur que son système redémarrera pour terminer l’installation du package. En cas de consentement explicite de l’utilisateur pour continuer, le package continue l’installation et <strong>changepk.exe</strong> exécute à l’aide de la clé de produit. L’utilisateur recevra une notification de rappel 30 secondes avant le redémarrage automatique. <br /> Après le redémarrage de l’appareil, le processus de mise à niveau d’édition se termine. L’utilisateur recevra une notification indiquant la réussite de la mise à niveau. <br /> ce nœud peut également être utilisé pour activer ou modifier une clé de produit sur une édition particulière de Windows 10 appareil de bureau en entrant une clé de produit. L’activation ou la modification d’une clé de produit ne nécessite pas de redémarrage et est un processus silencieux pour l’utilisateur.<br /><blockquote>[!Important]<br />la clé de produit entrée doit contenir 29 caractères (c’est-à-dire qu’elle doit inclure des tirets), sinon la modification de l’activation, de la mise à niveau de l’édition ou de la clé de produit sur Windows 10 appareils de bureau échoue. La clé de produit est acquise auprès du centre de gestion des licences en volume Microsoft. Votre organisation doit avoir un contrat de licence en volume avec Microsoft pour accéder au portail.</blockquote><br /> Voici les chemins de mise à niveau d’édition valides lors de l’utilisation de ce nœud via un MDM :<ul><li>Windows 10 Entreprise à Windows 10 Éducation</li><li>Windows 10 Famille à Windows 10 Éducation</li><li>Windows 10 Professionnel à Windows 10 Éducation</li><li>Windows 10 Professionnel à Windows 10 Entreprise</li></ul><br /> L’activation ou la modification d’une clé de produit peut être effectuée sur les éditions suivantes :<ul><li>Windows 10 Éducation</li><li>Windows 10 Entreprise</li><li>Windows 10 Famille</li><li>Windows 10 Professionnel</li></ul><br /> | 




 

### <a name="properties"></a>Propriétés

La **classe \_ WindowsLicensing MDM** a ces propriétés.

<dl> <dt>

[Édition](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent.

</dd> <dt>

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/ »

</dd> <dt>

[Statut](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine DMMap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

