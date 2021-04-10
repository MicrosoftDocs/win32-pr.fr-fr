---
description: Le compilateur SNMP s’exécute en tant que fichier exécutable unique dans le mode de ligne de commande.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210555"
---
# <a name="smi2smir"></a>smi2smir

Le compilateur SNMP s’exécute en tant que fichier exécutable unique dans le mode de ligne de commande. Le compilateur accepte un module d’informations SNMP comme entrée et accepte tous les modules supplémentaires nécessaires à la résolution des références externes. Utilisez l’un des exemples de syntaxe de ligne de commande suivants.

Pour plus d’informations sur l’utilisation de ce compilateur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>Commutateurs

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> <dd>

Le compilateur accepte les arguments de diagnostic suivants.

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _niveau de diagnostic_*_>_*
</dt> <dd>

Type de diagnostic à afficher. La valeur par défaut est 2.

La liste suivante répertorie les valeurs de niveau de diagnostic qui peuvent être définies :

-   0 = en mode silencieux
-   1 = irrécupérable
-   2 = fatal et avertissement
-   3 = messages fatals, d’avertissement et d’informations

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _nombre_*_>_*
</dt> <dd>

Nombre maximal de messages d’avertissement et d’erreur à afficher ; le *nombre* doit être un entier décimal positif. Si vous ne spécifiez pas **/c** , le nombre d’erreurs pouvant être signalées est illimité.

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> <dd>

Le compilateur accepte les arguments de version suivants.

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

Spécifie une conformité stricte à l’SMI SNMPv1. Le compilateur signale une erreur s’il détecte des instructions non-SNMPv1.

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

Spécifie une conformité stricte à l’SMI SNMPv2. Le compilateur signale une erreur s’il détecte des instructions non-SNMPv2.

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> <dd>

Le compilateur accepte les arguments de commande suivants.

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Supprime le module spécifié du stockage SMIR.

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

Supprime tous les modules dans le stockage SMIR.

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Répertorie tous les modules dans le stockage SMIR.

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

Effectue une vérification de la syntaxe locale sur le module.

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ce** **\[<** _CommandModifier_*_>\]_*
</dt> <dd>

Effectue des contrôles locaux et externes sur le module.

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*
</dt> <dd>

Effectue des contrôles locaux et externes et charge le module dans le stockage SMIR.

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa <** _CommandModifier_*_>\]_*
</dt> <dd>

Identique à **/a**, mais fonctionne en mode silencieux.

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*
</dt> <dd>

Génère un fichier stockage SMIR. mof que vous pouvez charger ultérieurement dans WMI à l’aide du compilateur MOF. Utilisé par le fournisseur de classes SNMP pour fournir dynamiquement des classes à un ou plusieurs espaces de noms. Utilisez cette option lorsque vous ne savez pas quelles MIB sont pris en charge par les périphériques SNMP gérés. Le fournisseur de classes SNMP vérifie l’appareil au moment de l’exécution pour la présence de ce MIB et fournit les classes de manière dynamique à l’espace de noms.

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*
</dt> <dd>

Génère un fichier. mof statique qui peut être chargé ultérieurement dans WMI en tant que classes statiques pour un espace de noms particulier. Utilisez cette option lorsque vous savez quelles MIB sont pris en charge par les périphériques SNMP gérés. Vous pouvez définir le fichier. mof à générer en dirigeant la sortie de votre commande vers un fichier spécifié. N’utilisez pas with **/ext/o**.

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> <dd>

Le compilateur accepte les modificateurs de commande suivants.

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _Directory_*_>_*
</dt> <dd>

Spécifie un répertoire dans lequel rechercher les modules MIB dépendants. Utilisez avec **/a**, **/ce**, **/g**, **/GC** et **/sa**. L’option **/i** peut apparaître plusieurs fois dans la commande ; les répertoires sont recherchés dans l’ordre spécifié dans la commande.

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/ch**
</dt> <dd>

Génère des informations de contexte, telles que la date, l’heure, l’hôte ou l’utilisateur, dans l’en-tête du fichier MOF. À utiliser avec **/g** et **/GC**.

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**commutateur**
</dt> <dd>

Génère des classes [SnmpNotification](snmpnotification.md) . Utilisez avec **/a**, **/g** et **/sa**.

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/ext**
</dt> <dd>

Génère des classes [SnmpExtendedNotification](snmpextendednotification.md) . Utilisez avec **/a**, **/g** et **/sa**.

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

Génère uniquement des classes [SnmpNotification](snmpnotification.md) . Utilisez avec **/a**, **/g** et **/sa**.

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

Génère uniquement des classes [SnmpExtendedNotification](snmpextendednotification.md) . Utilisez avec **/a**, **/g** et **/sa**.

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**commutateur**
</dt> <dd>

Ne mappe pas le texte de la clause DESCRIPTION. Utilisez avec **/a**, **/g**, **/GC** et **/sa**. Utilisez cette option lorsque vous souhaitez réduire les besoins de stockage.

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/Auto**
</dt> <dd>

Reconstruit la table de recherche MIB avant de terminer le commutateur <*CommandArg*>. Utilisez avec **/a**, **/ce**, **/g** et **/GC**.

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> <dd>

Le compilateur accepte les arguments de registre suivants.

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/pa**
</dt> <dd>

Ajoute le répertoire spécifié au registre. L'emplacement par défaut est le répertoire actif.

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/PD**
</dt> <dd>

Supprime le répertoire spécifié du Registre. L'emplacement par défaut est le répertoire actif.

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**/pl**
</dt> <dd>

Répertorie les répertoires de recherche MIB dans le registre.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Reconstruit l’intégralité de la table de recherche MIB.

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> <dd>

Le compilateur accepte les arguments d’informations de module suivants.

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Retourne le nom ASN. 1 du module spécifié.

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

Retourne les noms ASN. 1 de tous les modules d’importation référencés par le module d’entrée.

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> <dd>

Le compilateur accepte les arguments d’aide suivants.

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Affiche de l’aide sur la syntaxe du compilateur SNMP.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Affiche de l’aide sur la syntaxe du compilateur SNMP.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les modules d’informations SNMP sont écrits dans un sous-ensemble de la notation de syntaxe abstraite One (ASN. 1). le compilateur exécute les fonctions suivantes :

-   Charge les données à partir du module d’informations SNMP.
-   Effectue des opérations de vérification sur le module d’informations. Par exemple, il vérifie la syntaxe locale et vérifie les références externes par rapport aux informations contenues dans les modules subsidiaires.
-   Supprime toutes les données précédemment chargées du stockage SMIR ou supprime les données chargées à partir d’un module d’informations.
-   Retourne le nom du module ASN. 1 d’un fichier spécifié ou retourne le nom du module ASN. 1 de tous les modules importés dans un fichier spécifié.
-   Retourne les noms de module ASN.1 de tous les modules d’informations SNMP actuellement chargés dans le stockage SMIR.
-   Effectue une résolution automatique des modules importés au lieu de demander aux utilisateurs de spécifier manuellement les modules requis.
-   Exécute un mode de chargement en mode silencieux qui ne génère pas de sortie, mais peut être utilisé pour charger des données dans stockage SMIR pendant une opération d’installation.
-   Renvoie les données du module informations SNMP dans le stockage SMIR.
-   Crée éventuellement un fichier MOF statique ou stockage SMIR contenant la sortie du module information.

    Si nécessaire, vous pouvez charger le fichier. mof statique dans un espace de noms WMI. Un fichier stockage SMIR. mof contient le nom de l’espace de noms SNMP dans lequel les classes doivent résider.

## <a name="examples"></a>Exemples

L’exemple suivant définit le fichier PRA. mof comme sortie du fichier PRA. MIB.

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages d’erreur du compilateur SNMP](snmp-compiler-error-messages.md)
</dt> <dt>

[Configuration de l’environnement WMI SNMP](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[Accès aux appareils SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 




