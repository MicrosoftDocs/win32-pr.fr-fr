---
description: Prise en charge de l’exécution automatique
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Prise en charge de l’exécution automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467a4f6289492177beab0469a181297b13accfce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758457"
---
# <a name="supporting-autoplay"></a>Prise en charge de l’exécution automatique

La lecture automatique est une fonctionnalité de l’interpréteur de commandes qui lance des applications associées à des appareils particuliers. En fonction des paramètres de lecture automatique actuels, cette fonctionnalité effectue l’une des actions suivantes, telles que la présentation d’une liste d’applications de gestionnaire disponibles, l’affichage d’une vue de dossier standard de fichiers, et ainsi de suite.

Dans Windows Vista, la fonctionnalité d’exécution automatique a été étendue afin qu’un appareil WPD puisse fournir une liste de types de contenu pris en charge. De même, les applications WPD peuvent enregistrer les types de contenu qu’ils prennent en charge. Par exemple, un Assistant acquisition de photos peut s’inscrire en tant que gestionnaire pour tout appareil WPD fournissant des images, et une application multimédia peut s’inscrire en tant que gestionnaire pour tous les appareils qui stockent des fichiers audio ou vidéo.

Les applications enregistrent des informations spécifiques au gestionnaire en écrivant des entrées dans la clé de **\_ \_ \\ \\ \\ \\ \\ \\ \\ gestionnaires AutoplayHandlers de l’Explorateur Microsoft Windows CurrentVersion de l’ordinateur local** . En guise d’exemple d’utilisation d’un gestionnaire d’application WPD (nommé MyWpdApplication.exe), l’application peut insérer les valeurs suivantes sous la clé **\\ \\ MyWpdApplicationHandler des gestionnaires** .



| Valeur          | Type            | Données                                                 |
|----------------|-----------------|------------------------------------------------------|
| Action         | SZ de REG \_         | Parcourir le contenu sur des appareils mobiles.                  |
| CLSIDForCancel | SZ de REG \_         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ développer \_ SZ | % SystemDrive% de \\ fichiers \\ wpd multimédia \\MyWpdApplication.exe |
| InitCmdLine    | SZ de REG \_         | /AutoPlay                                            |
| ProgID         | SZ de REG \_         | MyWpdApplication.MyWpdApplicationAutoPlay            |
| Fournisseur       | SZ de REG \_         | MyWpdApplication                                     |



 

Pour plus d’informations sur les clés de registre de lecture automatique et les valeurs qui se trouvent sous la clé **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AUTOPLAYHANDLERS \\ handlers** , consultez la documentation correspondante sur MSDN.

### <a name="the-wpd-autoplay-scheme"></a>Schéma d’exécution automatique WPD

Le schéma d’exécution automatique WPD s’intègre à la fonctionnalité d’exécution automatique de Windows Vista. Pour ce faire, il prend en charge trois catégories d’exécution automatique, qui sont décrites dans le tableau suivant.



| Category | Description                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| Source   | Un appareil WPD peut être traité comme une source de contenu (autrement dit, le contenu peut être transféré à partir de l’appareil).        |
| Récepteur     | Un appareil WPD peut être traité comme destination du contenu (autrement dit, le contenu peut être transféré vers l’appareil).    |
| Fonction | Un appareil WPD prend en charge une fonctionnalité programmable ou contrôlable (par exemple, il peut envoyer et recevoir des messages SMS). |



 

Les applications s’inscrivent pour la catégorie source, récepteur et/ou fonction appropriée en écrivant des entrées dans la section d’exécution automatique du Registre système. Ces entrées s’affichent sous la clé de la clé wpd de l' **\_ \_ \\ \\ \\ \\ Explorateur Windows CurrentVersion \\ Explorer \\ AutoplayHandlers \\ EventHandlers \\ de l’ordinateur local** . Sous la clé WPD se trouvent la **fonction**, le **récepteur** et les clés **sources** . Sous chacune de ces clés se trouve un GUID qui correspond à une catégorie fonctionnelle ou à un type de contenu WPD.

Le tableau suivant répertorie les GUID trouvés sous la clé de **fonction** dans le registre et identifie la catégorie fonctionnelle qui correspond à chaque GUID.



| Catégorie fonctionnelle WPD                           | Clé de Registre (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| la \_ catégorie fonctionnelle wpd \_ \_ tout                    | {2D8A6512-A74C-448E-BA8A-F4AC07C49399} |
| \_ \_ \_ capture audio de la catégorie fonctionnelle wpd \_         | {3F2A1919-C7C2-4A00-855D-F57CF06DEBBB} |
| \_appareil de \_ catégorie \_ fonctionnelle wpd                 | {08EA466B-E3A4-4336-A1F3-A44D2B5C438C} |
| \_ \_ \_ Configuration réseau de la catégorie fonctionnelle wpd \_ | {48F4DB72-7C6A-4AB0-9E1A-470E3CDBF26A} |
| informations de rendu de la \_ catégorie fonctionnelle wpd \_ \_ \_ | {08600BA4-A7BA-4A01-AB0E-0065D0A356D3} |
| \_catégorie fonctionnelle \_ wpd \_ SMS                    | {0044A0B1-C1E9-4AFD-B358-A62C6117C9CF} |
| \_capture d' \_ \_ image continue \_ de la catégorie fonctionnelle wpd \_  | {613CA327-AB93-4900-B4FA-895BB5874B79} |
| \_stockage des \_ catégories FONCTIONNELLEs wpd \_                | {23F05BBC-15DE-4C2A-A55B-A9AF5CE412EF} |
| \_ \_ \_ capture vidéo de la catégorie fonctionnelle wpd \_         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

Le tableau suivant répertorie les GUID trouvés sous le **récepteur** et les clés **sources** dans le registre, et identifie le type de contenu qui correspond à chaque GUID.



| Type de contenu WPD                          | Clé de Registre (GUID)                    |
|-------------------------------------------|----------------------------------------|
| \_type de contenu wpd \_ \_ tout                   | {80E170D2-1055-4A3E-B952-82CC4F8A8689} |
| \_ \_ rendez-vous de type de contenu wpd \_           | {0FED060E-8793-4B1E-90C9-48AC389AC631} |
| \_type de contenu wpd \_ \_ audio                 | {4AD2C85E-5E2D-45E5-8864-4F229E3C6CF0} |
| TYPE de contenu WPD- \_ \_ \_ \_ album audio          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| \_calendrier du \_ type de contenu wpd \_              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| \_certificat de \_ type de contenu wpd \_           | {DC3876E8-A948-4060-9050-CBD77E8A3D87} |
| \_contact de \_ type de contenu wpd \_               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| \_groupe de \_ contacts du type de contenu wpd \_ \_        | {346B8932-4C36-40D8-9415-1828291F9DE9} |
| \_document de \_ type de contenu wpd \_              | {680ADF52-950A-4041-9B41-65E393648155} |
| \_e-mail de \_ type de contenu wpd \_                 | {8038044A-7E51-4F8F-883D-1D0623D14533} |
| \_dossier de \_ type de contenu wpd \_                | {27E2E392-A111-48E0-AB0C-E17705A05F85} |
| \_ \_ objet fonctionnel du type de contenu wpd \_ \_    | {99ED0160-17FF-4C44-9D98-1D7A6F941921} |
| \_ \_ fichier générique du type de contenu wpd \_ \_         | {0085E0A6-8D34-45D7-BC5C-447E59C73D48} |
| \_ \_ message générique du type de contenu wpd \_ \_      | {E80EAAF8-B2DB-4133-B67E-1BEF4B4A6E5F} |
| \_image de \_ type de contenu wpd \_                 | {EF2107D5-A52A-4243-A26B-62D4176D7603} |
| \_album d' \_ images de type de contenu wpd \_ \_          | {75793148-15F5-4A30-A813-54ED8A37E226} |
| \_type de contenu wpd \_ \_ \_ diffusion multimédia           | {5E88B3CC-3E65-4E62-BFFF-229495253AB0} |
| \_mémo de \_ type de contenu wpd \_                  | {9CD20ECF-3B50-414F-A641-E473FFE45751} |
| TYPE de contenu WPD- \_ \_ \_ album de \_ contenu mixte \_ | {00F0C3AC-A593-49AC-9219-24ABCA5A2563} |
| \_Association de \_ réseau de type de contenu wpd \_ \_  | {031DA7EE-18C8-4205-847E-89A11261D0F3} |
| \_playlist de \_ type de contenu wpd \_              | {1A33F7E4-AF13-48F5-994E-77369DFE04A3} |
| \_programme de \_ type de contenu wpd \_               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| \_section du \_ type de contenu wpd \_               | {821089F5-1D91-4DC9-BE3C-BBB1B35B18CE} |
| \_tâche de \_ type de contenu wpd \_                  | {63252F2C-887F-4CB6-B1AC-D29855DCEF6C} |
| \_télévision du \_ type de contenu wpd \_            | {60A169CF-F2AE-4E21-9375-9677F11C1C6E} |
| \_type de contenu wpd \_ \_ non spécifié           | {28D8D31E-249C-454E-AABC-34883168E634} |
| vidéo sur le \_ type de contenu wpd \_ \_                 | {9261B03C-3D78-4519-85E3-02C5E1F50BB9} |
| \_ \_ album vidéo de type de contenu wpd \_ \_          | {012B0DB7-D4C1-45D6-B081-94B87779614F} |
| \_profil de type de contenu wpd \_ \_ sans fil \_     | {0BAC070A-9F5F-4DA4-A8F6-3DE44D68FD6C} |



 

Si une application prenait en charge une fonction particulière, une source ou une catégorie de récepteur, elle insérerait une chaîne spécifiant le nom de la clé de gestionnaire sous le GUID qui a identifié la catégorie fonctionnelle ou de type de contenu prise en charge. À l’aide de MyWpdApplication comme exemple, l’application crée une entrée sous le... Clés **/EventHandlers/wpd/Function**, **/Sink** ou **/source** . Cette entrée se présente sous la forme « MyWpdApplicationHandler » et est de type REG \_ sz. En outre, cette entrée apparaît sous le GUID pour les catégories fonctionnelles ou les types de contenu pris en charge par l’application.

 

 



