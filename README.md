# Gestion de la Base de Données d'un Hôtel

## Contexte
Après la construction de ses hôtels dans une des zones touristiques, un directeur souhaite préparer une base de données pour faciliter la gestion de ses données.

Le directeur vous a présenté les informations suivantes à travers le modèle de relation entre entités :

![Modèle de Relation Entre Entités](https://i.imgur.com/oHkrfiJ.png)

## Instructions
Convertir le modèle de relations entre entités en un diagramme relationnel.

## Solution
Voici la transformation du modèle de relation entre entités en un schéma relationnel :

### Tables et leurs attributs

#### **Hotel**
- `Hotel_Id` 
- `Hotel_Name`

#### **Type**
- `Type_Id` 
- `Type_Name`

#### **Room**
- `Room_Id` 
- `Floor`
- `Hotel_Id`
- `Type_Id` 

#### **Category**
- `Category_Id` 
- `Category_Name`
- `Price`
- `Beds_Numbers`

#### **Employee**
- `Employee_Id` 
- `Employee_Name`
- `Employee_Speciality`

### Relations entre les tables

#### **Works** (Relation entre `Employee` et `Hotel`)
- `Employee_Id` 
- `Hotel_Id` 

#### **Leads** (Auto-relation `Employee`)
- `Leader_Id`
- `Employee_Id`

#### **Room_Category** (Relation entre `Room` et `Category`)
- `Room_Id` 
- `Category_Id` 

---

Ce fichier README sert de référence pour comprendre la structure de la base de données et son schéma relationnel.