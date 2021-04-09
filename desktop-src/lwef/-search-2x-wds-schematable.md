---
title: Schéma (fonctionnalités héritées de l’environnement Windows)
description: Le schéma documente les valeurs et les propriétés utilisées par l’index pour stocker les données à des fins d’indexation ou de tri.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a122959b007ba4d4434e65b53fc2e330857cafe
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "104030911"
---
# <a name="schema"></a>schéma

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

Le schéma documente les valeurs et les propriétés utilisées par l’index pour stocker les données à des fins d’indexation ou de tri. Le tableau schéma répertorie les colonnes et leurs propriétés (type et propid) incluses dans le schéma pour Microsoft Windows Desktop Search (WDS) 2.6.5.

## <a name="schema"></a>schéma



| Nom de la colonne                  | Description                                                                                                             | Propid                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Commentaires                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Créer                       | Date et heure de création du fichier                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Dossier convivial pour l’élément                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Auteur du document                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | Category                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | Mots clés                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Préfixe de l’objet (Re :, FW :, etc.)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | Intitulé                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | Description conviviale du type de fichier à partir du Registre (par exemple, le fichier de requête >.                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | Nom du dossier parent                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/nom_dossier                   |
| IsAttachment                 | Indique que l’élément est une pièce jointe                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsAttachment                 |
| IsDeleted                    | Indique que l’élément est marqué pour suppression (corbeille, éléments supprimés, etc.)                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsDeleted                    |
| LastViewed                   | Date à laquelle l’élément a été affiché pour la dernière fois par l’utilisateur                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| Personnes                       | Personnes impliquées dans cet élément                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/personnes                       |
| PerceivedType                | PerceivedType de l’objet NOTE : il s’agit uniquement d’une récupération.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | Nom complet du PerceivedType.Jamais affiché ou interrogé                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| PrimaryDate                  | Date la plus intéressante (heure de la dernière écriture des fichiers, date de réception de l’e-mail)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryDate                  |
| Taille                         | Taille d’un fichier.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Objet du fichier. Remarque : actuellement, les objets de messagerie sont mappés à PrimaryTitle aujourd’hui et ne sont pas dupliqués en raison de leur longueur | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | URL basée sur une requête                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| Write                        | Date et heure de la dernière écriture dans le fichier                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Date d’échéance d’un élément                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| IsIncomplete                 | Indique que l’élément n’est pas entièrement disponible                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsIncomplete                 |
| IsFlaggedCompleted           | Indique que l’élément est marqué comme terminé                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| IsFlagged                    | Indique que l’élément est marqué d’un indicateur                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlagged                    |
| FlagText                     | Texte affiché pour l’indicateur, par exemple, révision, suivi, etc.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| Identité                     | Identité pour les utilisateurs de OE                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/identité                     |
| IsRead                       | Indique que l’élément a été lu                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRead                       |
| importance                   | Importance ou priorité MAPI                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/importance                   |
| ContainerHash                | Code de hachage qui identifie les pièces jointes à supprimer en fonction d’une URL de conteneur commune                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| DocFormat                    | Format de document ou MIMETYPE (par exemple « Message/RFC822 » pour un fichier EML)                                              | 0B63E350-9CCC-11D0-BCDB-00805FCCCE04/5                            |
| GatherTimeModified           | Heure à laquelle l’indexeur a analysé le document pour la dernière fois pour la mise à jour du catalogue                                                           | 0b63e350-9ccc-11D0-bcdb-00805fccce04/4                            |
| Magasin                        | Le magasin ou le gestionnaire de protocole (FILE, MAIL, OUTLOOKEXPRESS)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Store                        |
| FileExt                      | Extension de fichier                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | Nom du fichier.                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| NomCourt                    | Short (8,3) nom de fichier du fichier                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| AttachmentNames              | Noms des pièces jointes dans un message                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AttachmentNames              |
| BccAddress                   | Adresses dans le champ Cci :                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | Noms des personnes dans le champ Cci :                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Adresses dans le champ cc :                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Noms de personnes dans le champ cc :                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| ConversationID               | ID unique d’une conversation dans des threads de messagerie                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ConversationID               |
| FromAddress                  | Adresses dans le champ de :                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Nom de la personne dans le champ de :                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | Indique que le courrier a été répondu à ou transféré ( \_ action cdoPR = 261 262)                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | Indique que le courrier électronique a une pièce jointe (T ou F)                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| ReceivedDate                 | Heure de remise                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/date de provenance                 |
| ToAddress                    | Adresses dans le champ à :                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToAddress                    |
| ToName                       | Noms de personnes dans le champ à :                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToName                       |
| TaskStatus                   | État d’une tâche                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | Heure de fin (généralement pour les réunions/événements)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| IsRecurring                  | Indique que l’élément est périodique (par exemple, les réunions)                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | Heure de début (généralement pour les réunions/événements)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Duration                     | Durée de la réunion en minutes                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/durée                     |
| Emplacement                     | Emplacement où l’élément (par exemple, une réunion) se produit                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/emplacement                     |
| Ans                  | Date anniversaire                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/anniversaire                  |
| AssistantName                | Nom de l’Assistant                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | Téléphone de l’Assistant                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Birthday                     | Anniversaire du contact                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/anniversaire                     |
| BusinessAddressCity          | Informations sur l’adresse professionnelle                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | Informations sur l’adresse professionnelle                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | Informations sur l’adresse professionnelle                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | Informations sur l’adresse professionnelle                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressStreet        | Informations sur l’adresse professionnelle                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressStreet        |
| BusinessAddressCountry       | Informations sur l’adresse professionnelle                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | Rappeler les informations téléphoniques                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | Informations téléphoniques                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | Noms des enfants pour le contact                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/enfants                     |
| CompanyMainTelephone         | Informations téléphoniques                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | Nom de l’e-mail du contact                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | Nom complet de l’adresse de messagerie                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| FirstName                    | Prénom du contact                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Nom complet du contact                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Sexe                       | Mâle/femelle/autre                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/sexe                       |
| Cran                        | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Hobby                        |
| HomeAddressCity              | Informations sur l’adresse personnelle                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Informations sur l’adresse personnelle                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | Informations sur l’adresse personnelle                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | Informations sur l’adresse personnelle                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressStreet            | Informations sur l’adresse personnelle                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressStreet            |
| HomeFaxNumber                | Infos sur les télécopies                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | Infos sur les télécopies                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | Informations téléphoniques                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| Imadresse                    | Infos sur les messages instantanés                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/inaddress                    |
| JobTitle                     | Poste du contact                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | Informations téléphoniques                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/surnom                     |
| Office                       | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Bureau                       |
| OfficeTelephone              | Informations téléphoniques                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | Informations téléphoniques                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| LastName                     | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/nom                     |
| PersonalTitle                | Titre de la profession (Dr, Mr., Mme, Mme)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | Informations téléphoniques                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/profession                   |
| Époux                       | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/époux                       |
| Suffixe                       | Informations de contact                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/suffixe                       |
| TelexNumber                  | Info télex                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | Informations TTY/TDD                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | Page Web de contact                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/page Web                      |
| DocCompany                   | Company                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | Utilisateur du dernier enregistrement du document wa par                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | Dernière impression                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | Diapositives                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | Débit moyen des données en Kbits/s pour le fichier audio                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | Longueur en millisecondes du fichier audio                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | Nom de l’album                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | Nom de l’artiste                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | Genre de l’album                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | Nombre de pistes dans l’album                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | Année pendant laquelle l’album a été enregistré                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | Fabricant de l’appareil photo                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | Modèle d’appareil photo                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | FILETIME de données prises                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientation                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | Dimensions de l’image                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | Résolution X pour l’image                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResY                    | Résolution Y de l’image                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | Hauteur du frame du flux vidéo                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | Fréquence d’images en images par milliseconde pour le flux vidéo                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | Largeur du cadre pour le flux vidéo                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| Classe                        | Nom de classe                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/classe                        |
| Fonction                     | Nom de la fonction                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/Func                         |
| Structure                       | Nom de la structure                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/struct                       |
| Interface                    | Nom de l’interface                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/interface                    |
| Délégué                     | Nom du délégué                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/délégué                     |
| Propriété                     | Nom de la propriété                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/propriété                     |
| Énumération                         | Nom de l’enum                                                                                                               | 8dee0300-16c2-101B-B121-08002b2ecda9/enum                         |
| Const                        | Nom const                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/const                        |
| Événement                        | Nom d'événement                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/événement                        |
| Champ                        | Nom du champ                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/champ                        |
| Définir                       | Définir le nom                                                                                                             | 8dee0300-16c2-101B-B121-08002b2ecda9/def                          |
| Composant                    | Nom du composant                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/composant                    |
| Project                      | Nom du projet                                                                                                            | 8dee0300-16c2-101B-B121-08002b2ecda9/projet                      |
| Solution                     | Nom de la solution                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/solution                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Développement de compléments IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Développement de gestionnaires de protocole](-search-2x-wds-phaddins.md)
</dt> <dt>

[Syntaxe de requête avancée](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Types perçus](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 




