---
description: 'WsdCodeGen a deux fonctions : la génération de fichiers de configuration et la génération de code source pour le client WSDAPI et les applications hôtes.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Syntaxe de la ligne de commande WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863750"
---
# <a name="wsdcodegen-command-line-syntax"></a>Syntaxe de la ligne de commande WsdCodeGen

WsdCodeGen a deux fonctions : la génération de fichiers de configuration et la génération de code source pour le client WSDAPI et les applications hôtes. Cette rubrique indique la syntaxe de ligne de commande utilisée pour effectuer chaque tâche.

## <a name="generating-a-configuration-file"></a>Génération d’un fichier de configuration

### <a name="syntax"></a>Syntaxe

**WSDCODEGEN.EXE** **/generateconfig :**{**client** \| **Host** \| **All**} **\[ /outputfile :**_ConfigFileName_ *_\]_* *WSDLFileNameList*

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig : {client \| host \| All}**
</dt> <dd>

Type de code généré par le fichier de configuration de sortie. **/generateconfig : le client** est utilisé pour générer un fichier de configuration pour générer le code client, **/generateconfig : Host** est utilisé pour générer un fichier de configuration pour la génération de code hôte, et **/generateconfig : All** est utilisé pour générer un fichier de configuration pour la génération du code client et du code hôte.

</dd> <dt>

<span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile :**_ConfigFileName_
</dt> <dd>

Ce paramètre facultatif est utilisé pour spécifier le nom de fichier du fichier de configuration de sortie. Si ce paramètre est exclu, le nom du fichier de configuration de sortie est codegen.config.

</dd> <dt>

<span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*
</dt> <dd>

Incluez un modèle PnP-X dans le fichier de configuration.

</dd> <dt>

<span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*
</dt> <dd>

Liste délimitée par des espaces des fichiers WSDL à traiter par WsdCodeGen.

</dd> </dl>

## <a name="generating-source-code"></a>Génération du code source

### <a name="syntax"></a>Syntaxe

**WSDCODEGEN.EXE** **/GenerateCode** **\[ /download \]** **\[ /GBC \]** **\[ outputroot :**_chemin_ *_\]_* **\[ /WriteAccess :**_commande_ *_\]_* *nomdefichierdeconfiguration*

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**
</dt> <dd>

Indique à WsdCodeGen de générer le code source. Il s’agit du mode par défaut si aucun mode n’est spécifié.

</dd> <dt>

<span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**
</dt> <dd>

Télécharge les documents importés référencés par le fichier de configuration. Ce paramètre est facultatif.

</dd> <dt>

<span id="_gbc"></span><span id="_GBC"></span>**/gbc**
</dt> <dd>

Ajoute des commentaires au code source qui indique que le code a été généré. Ces commentaires sont précédés de l’expression « généré par ». Ce paramètre est facultatif.

</dd> <dt>

<span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot :**_chemin d’accès_
</dt> <dd>

Emplacement de sortie pour les fichiers générés. le *chemin d’accès* peut être un chemin d’accès absolu ou relatif. Ce paramètre est facultatif.

</dd> <dt>

<span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/WriteAccess :**_commande_
</dt> <dd>

Indique à WsdCodeGen d’exécuter la commande spécifiée avant de modifier les fichiers existants sur le disque. Les fichiers de sortie qui sont identiques à ceux du disque ne reçoivent pas cette commande et ne sont pas écrits dans. Si la commande contient la séquence « {0} », cette séquence sera remplacée par le nom du fichier à modifier. Si ce n’est pas le cas, le nom de fichier est ajouté à la commande.

Exemples :

**/WriteAccess : "attrib-r"**

**/WriteAccess : "attrib-r {0} "**

**/WriteAccess : «copier {0} .. \\ sauvegarde \\ »**

</dd> <dt>

<span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Nomdefichierdeconfiguration*
</dt> <dd>

Nom du fichier de configuration à traiter avant de générer le code.

</dd> </dl>

## <a name="formatting-legend"></a>Légende de mise en forme



| Format                                                                    | Signification                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| *Italique*                                                                  | Informations que l’utilisateur doit fournir                  |
| **Gras**                                                                  | Éléments que l'utilisateur doit taper exactement comme indiqué       |
| Entre crochets ( \[ \] )                                                   | Éléments facultatifs                                          |
| Entre accolades ( {} ); choix séparés par une barre verticale ( \| ). Exemple : {même \| impair} | Ensemble de choix à partir duquel l’utilisateur ne doit en choisir qu’un seul |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration WsdCodeGen](wsdcodegen-configuration-file.md)
</dt> <dt>

[Utilisation de WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 




